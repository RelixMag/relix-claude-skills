---
name: email-processor
description: Turn raw ticket-buyer / venue export files (CSV or XLSX — BBNY, Bearsville, GarciasCHI, Dayglo/Ruthie/Homestead, CapitolTheatre, and similar) into Beehiiv-ready import CSVs. Use this skill whenever the user mentions processing a ticket buyer file, a venue export, a "_OG" source file, an email upload, a Beehiiv import/List/Signup Source/Artist tag, or references any known List name (BBNY, Bearsville, CapitolTheatre, FANS.COM, GMP-MIA, GMP-NOLA, Hubspot, Jerry Dance Party, RelixAllSubs, RRPH, GarciasCHI, BBLV, BBNash, Dayglo) even if they don't say "Beehiiv" explicitly — e.g. "here's this quarter's BBNY file", "clean up this venue CSV for the mailing list", "combine these Ruthie Bandit files into Dayglo". Always check this skill before manually re-deriving column mappings or state/zip cleaning rules from scratch.
---

# Email Processor: Ticket-Buyer → Beehiiv Import

This skill turns messy, inconsistently-formatted ticket-buyer exports into
clean, deduplicated CSVs ready to import into Beehiiv. The rules here come
from real processing history across many venues and quarters — they exist
because each one fixed a real problem (a venue with no headers, a zip column
that was silently ignored for a year, Canadian postal codes that don't fit a
US zip pattern, and so on). Read `references/field_values.md` for the full
list of valid field values and the reasoning behind the less-obvious rules.

## Why a script, not manual processing

Every file needs the same handful of judgment-free transforms — dedup,
header mapping, state/country normalization — applied identically. Doing
this by hand or reasoning through it fresh each time is where inconsistencies
creep in (a missed bounce filter, a zip left as a float, a header alias
that's almost-but-not-quite right). `scripts/process_ticket_buyers.py`
encodes all of it deterministically, validated byte-for-byte against real
previously-processed files (BBNY Q2 2026, Dayglo Q2 2026). Use it rather than
re-deriving the transform each time — but still read the output summary and
spot-check a few rows, since new source files sometimes need a new header
alias or expose a rule this skill doesn't cover yet (see "When something
doesn't fit" below).

## Workflow

1. **Identify the new source file(s).** They usually arrive attached to an
   email or dropped in the project's Email Uploads folder, without any
   naming convention applied yet.

2. **Rename the original source file(s).** Append `_OG` before the extension
   (keep the original extension): `20260402_Bearsville_TicketBuyers_2026Q1_OG.csv`.
   Never rename or modify a file that already has `_OG` or `_UPLOADED` in its
   name without discussing it with the user first — those are treated as
   finalized.

3. **Work out the List, Signup Source, and Artist values.**
   - **List** is derived from the venue/source, e.g. `BBNY`, `Bearsville`,
     `Dayglo`. If the file doesn't clearly match one of the known List values
     in `references/field_values.md`, ask the user before inventing a new
     one — List values need sign-off.
   - **Signup Source** defaults to `Ticket Buyer` unless the file indicates
     otherwise (e.g. `Contest`, `Shop`).
   - **Artist** is freeform — set it only when the show/event specifically
     features that artist (a venue name alone, like GarciasCHI, is not an
     artist). Don't block on an unrecognized Artist value; it doesn't need
     confirmation the way List does.

4. **Detect the file's format** and pick the right `--format` for the script:
   - `xlsx-nohdr` — a no-header XLSX with fixed column positions (BBNY's
     historical format: event code, ticket ID, Last Name, First Name, email,
     Zip Code in columns 0–5). This is the default for any `.xlsx` file, so
     you usually don't need to pass `--format` explicitly for this case.
   - `xlsx-headers` — an XLSX **with** a header row (e.g. a CEG "Customer
     Contacts Report" export with columns like Account/Customer/Email/Phone/
     Address 1/Address 2/Address 3/City/State/ZIP/Status). Pass
     `--format xlsx-headers` explicitly — it's not auto-detected, since plain
     `.xlsx` defaults to the no-header case above.
   - `csv-headers` — any CSV with a header row, regardless of what the
     headers are literally called (the script fuzzy-matches common variants:
     firstName/first_name/"First Name", zip/postalCode/"Zip Code", etc.) This
     is the default for `.csv` files.
   - If a file doesn't match any of these three shapes, don't force it — flag
     it to the user and work out the mapping together rather than guessing.

5. **Run the mapper** for each source file:
   ```
   python3 scripts/process_ticket_buyers.py map <input_file> \
       --list <List> --signup-source "<Signup Source>" --artist "<Artist>" \
       [--format xlsx-headers] \
       --output <output.csv>
   ```
   Read the printed summary (rows written, skipped-no-email, skipped-dupe)
   and sanity-check it against the row count of the source file.

6. **Combining multiple sources into one List** (e.g. Dayglo, which pools
   several ticket-buyer files under different Artist tags): run `map` once
   per source file into a temp file with its own `--artist` value, then
   `merge` them, which dedupes by email across *all* sources combined (not
   just within each source):
   ```
   python3 scripts/process_ticket_buyers.py merge file1_mapped.csv file2_mapped.csv \
       --output <combined>.csv
   ```
   If more files come in later for an existing combined List, they can be
   merged into a fresh combined export the same way — mapped individually,
   then merged together with the prior sources' mapped output.

7. **Name the final output file** using
   `YYYYMMDD_LIST_SignupSource_ReportTimeframe_UPLOADED.csv`, e.g.
   `20260402_Bearsville_TicketBuyers_2026Q1_UPLOADED.csv`. `YYYYMMDD` is the
   processing date, `ReportTimeframe` is the period the source data covers
   (e.g. `2026Q1`) — ask the user if this isn't clear from context.

8. **Never silently overwrite a previously processed file.** If a change
   would touch an existing `_OG` or `_UPLOADED` file, say so and confirm
   before making it.

## What the script already handles for you

- Dedup by email (first occurrence wins), case-insensitive.
- Drops rows with no email.
- Lowercases all emails.
- Drops bounced/unsubscribed rows when a recognizable column is present.
- Converts full US state names and Canadian province names to 2-letter
  codes; leaves other international values as-is.
- Converts full/alpha-3 country names to 2-letter ISO codes.
- BBNY's zip column cleaning (zero-pads short numeric zips, truncates
  zip+4 to 5 digits, blanks 6–9 digit numeric garbage, uppercases
  alphanumeric UK/Canadian postal codes).
- Splits a combined `"LAST,FIRST"` name column (seen in CEG-style reports)
  into separate First/Last fields.
- Defaults a blank Country Code to `US` **only** when the State field
  clearly identifies a US (non-Canadian) jurisdiction — this was added after
  finding that some already-published files defaulted every blank country to
  US regardless of state, mislabeling a handful of genuinely Canadian
  addresses (Toronto/Ontario) as US. If you're re-processing an older file
  and its Country Code differs slightly from what's already published, this
  is why — the new value is the more correct one.

## When something doesn't fit

If a new source file has a shape the script doesn't recognize — a header
alias it's missing, a positional layout that isn't BBNY's, an unfamiliar
bounce/unsubscribe column name — don't force the existing formats onto it.
Open `scripts/process_ticket_buyers.py`, find `HEADER_ALIASES` (for header-
based files) or `load_xlsx_nohdr` (for positional files), and extend it, then
re-run. This is expected to happen as new venues show up; it's cheaper to
extend the script once than to re-derive the mapping by hand every time that
venue sends a new file.
