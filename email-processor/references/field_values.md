# Beehiiv Field Reference

Full reference for valid values and field mapping used by
`scripts/process_ticket_buyers.py`. Read this when: a new file needs a List
value you don't recognize, you need to know the exact Beehiiv header
capitalization, or you're extending the script for a new source format.

## Beehiiv field names (exact capitalization matters)

| Beehiiv Field    | Typical source column names                          |
|-------------------|--------------------------------------------------------|
| First Name         | first name, firstName, Customer (combined, split on comma) |
| Last Name          | last name, lastName, Customer (combined, split on comma)   |
| email              | email, Email                                            |
| Phone Number        | phone, Phone Number, phoneNumber                        |
| Street Address      | address, Street Address, address1, Address 1            |
| Address Line 2      | address2, Address Line 2, Apt/Suite, Address 3 (used only if Address Line 2 is empty) |
| City Name           | city, City Name                                         |
| State               | state                                                    |
| Zip Code            | zip, postal_code, Zip Code, postalCode, ZIP              |
| Country Code        | country, country code                                    |
| List                | set per file (not read from source)                      |
| Signup Source       | set per file (not read from source)                      |
| Artist              | set per file (not read from source)                      |

Output column order (matches the convention already established across
every previously-processed file):
`First Name, Last Name, email, Phone Number, Street Address, Address Line 2, City Name, State, Zip Code, Country Code, List, Signup Source, Artist`

## Valid List values

`BBNY, Bearsville, CapitolTheatre, FANS.COM, GMP-MIA, GMP-NOLA, Hubspot, Jerry Dance Party, RelixAllSubs, RRPH, GarciasCHI, BBLV, BBNash, Dayglo`

**New List values need sign-off before use** — this is the one field where
you should confirm with the user rather than inventing a value, because List
is how downstream Beehiiv segments/campaigns are built.

## Valid Signup Source values

`Contest, Ticket Buyer, Shop, Meta, Signup_Contests, Relix.com`

Defaults to `Ticket Buyer` for venue ticket-buyer exports unless the file
indicates otherwise.

## Artist tag

**Freeform — not restricted to a fixed list** (confirmed 2026-07-01). Set it
only when the show/event specifically features that artist; a venue name
alone (e.g. GarciasCHI) is not an artist tag. Previously used values:
`Artist_BillyStrings, Artist_Goose, Artist_GratefulDead, Artist_StringCheeseIncident, Artist_widespreadPanic, RuthieBandit, Homestead`.
Unlike List, a new Artist value doesn't need confirmation before use.

## Output file naming

- Original source file, on receipt: append `_OG` before the extension, keep
  the original extension. Example: `20260402_Bearsville_TicketBuyers_2026Q1_OG.csv`
- Processed/final file: `YYYYMMDD_LIST_SignupSource_ReportTimeframe_UPLOADED.csv`
  (e.g. `20260402_Bearsville_TicketBuyers_2026Q1_UPLOADED.csv`). Always CSV,
  regardless of the source file type.
  - Note: an earlier version of this rules doc said the suffix should be
    `_UPLOAD` (no "-ED"), but every file actually produced uses `_UPLOADED` —
    that's the convention to follow going forward.
- Never modify a previously processed (`_OG` or `_UPLOADED`) file without
  discussing the change with the user first.

## Source file formats

### `xlsx-nohdr` — positional, no header row (BBNY)

Column positions: 0 = event code (ignored), 1 = ticket ID (ignored),
2 = Last Name, 3 = First Name, 4 = email, 5 = Zip Code.

**Country Code is left blank for BBNY** — there's no country column, and
this was an explicit decision (confirmed 2026-07-08) not to infer it from
postal code format, and this format is exempt from the zip-shape-based
Country Code default described below (confirmed 2026-08-05).

## Zip Code cleaning (applies to every format)

Originally written for BBNY's positional column 5 (confirmed 2026-07-08 —
that column was silently ignored for over a year before someone noticed it
was ~70% populated and worth cleaning up), but the rules aren't actually
BBNY-specific. As of 2026-08-05 they apply to the `Zip Code` field for
**every** source format (`csv-headers`, `xlsx-headers`, and `xlsx-nohdr`),
since header-based exports (e.g. Klaviyo-style CSV exports) had the exact
same zip+4 / leading-zero problems and were previously left uncleaned:
- Pure numeric, ≤5 digits → zero-pad to 5 digits (handles zips that lost a
  leading zero, common with Excel treating zips as numbers)
- Pure numeric, `XXXXX-XXXX` format → truncate to the first 5 digits
- Pure numeric, 6–9 digits, no dash → invalid data entry, blank it out
- Contains letters (UK/Canadian postal codes) → keep, uppercase, normalize
  whitespace
- Anything else that doesn't match one of the above (e.g. a stray space
  like `"021 31"`) → preserve as-is rather than discard real data

### `xlsx-headers` — XLSX with a header row (e.g. CEG "Customer Contacts Report")

Seen on the Dayglo/Ruthie Bandit after-party files. Typical columns:
`Account, Customer, Event, Event Time, Email, Phone, Address 1, Address 2, Address 3, City, State, ZIP, Status`.
`Customer` is a combined `"LAST,FIRST"` field that gets split into First/Last
Name. `Status` is checked for bounce/unsubscribe keywords if populated.

### `csv-headers` — any CSV with a header row (GarciasCHI, Bearsville, Homestead, etc.)

Headers vary by source; mapped by fuzzy name match (case/spacing/
underscore-insensitive) rather than an exact string, since every venue
spells these slightly differently.

## Multi-source Lists (e.g. Dayglo)

Dayglo was added 2026-07-01 to combine ticket-buyer contacts from multiple
unrelated source files into one List, each tagged with its own Artist value —
`RuthieBandit` (three CEG "Customer Contacts Report" files for the Goose
After-Party ft. Ruthie Bandit events, 6/19–6/20/2026) and `Homestead` (from a
"Homestead Buyers Email List.csv"). This is the pattern `merge` is for: map
each source individually with its own `--artist`, then merge them into one
deduped-by-email export. If more files come in for the same combined List
later, map and merge them in the same way, alongside the already-published
mapped sources.

## A note on Country Code defaulting

The script defaults a blank Country Code to `US` in two steps, run in order:

1. If the State field normalizes to a recognized **US** (non-Canadian)
   code, default Country Code to `US`. This was a deliberate choice, not an
   arbitrary one: comparing this script's output against the
   already-published Dayglo file byte-for-byte turned up 7 rows where a
   Toronto/Ontario address had been tagged `Country Code = US` — apparently
   an earlier processing pass defaulted every blank country to US without
   checking the state. This script's state-aware default avoids repeating
   that mistake.
2. **(Added 2026-08-05)** If Country Code and State are *both* still blank
   (common on files like Klaviyo-style exports that have no State/Country
   column at all, only a Zip Code), and the cleaned Zip Code is a plain
   5-digit number, default Country Code to `US`. Canadian postal codes are
   alphanumeric (e.g. `M5V 3L9`) and never match a plain 5-digit pattern, so
   this doesn't reintroduce the Toronto/Ontario mislabeling problem from
   step 1 — it only fires when there's no state at all to have gotten wrong.
   This step is **skipped for BBNY** (`xlsx-nohdr`), which keeps its
   explicit, documented decision to leave Country Code blank regardless of
   zip shape.

If you re-process an older file, don't be surprised if a handful of
Country Code values change from what was previously published — the new
values are the corrected ones.

## Change log

| Date       | Rule Added / Changed                                                        |
|------------|-------------------------------------------------------------------------------|
| 2026-04-02 | Initial rules established (BBNY file)                                        |
| 2026-04-02 | Field names must match Beehiiv exact capitalization                          |
| 2026-04-02 | Convert state names to 2-letter codes                                        |
| 2026-04-02 | Convert country names to 2-letter ISO codes                                  |
| 2026-04-02 | Exclude bounced and unsubscribed contacts                                    |
| 2026-04-02 | Source files suffixed `_OG` on receipt                                       |
| 2026-04-02 | Never modify previously processed files without discussion first             |
| 2026-07-01 | Added "Dayglo" as a valid List value; multi-source-per-List pattern established |
| 2026-07-01 | Artist field confirmed freeform (no fixed list)                              |
| 2026-07-08 | BBNY XLSX col 5 identified as Zip Code (previously ignored); cleaning rules added; Country Code left blank for BBNY |
| 2026-08-05 | Corrected output suffix to `_UPLOADED` (docs previously said `_UPLOAD`, but every real file used `_UPLOADED`) |
| 2026-08-05 | Added `xlsx-headers` format for CEG-style header-based Excel exports, with combined-name splitting |
| 2026-08-05 | Made Country Code default state-aware (US only when State is a non-Canadian US code), after finding the prior blanket default had mislabeled Canadian addresses as US in the published Dayglo file |
| 2026-08-05 | Added `emailmarketingconsent` (Klaviyo-style "Email Marketing Consent" column: SUBSCRIBED/NEVER_SUBSCRIBED/UNSUBSCRIBED) as a recognized `_status` header alias, so UNSUBSCRIBED rows get filtered like any other unsub column |
| 2026-08-05 | Generalized Zip Code cleaning (zero-pad, truncate zip+4, blank 6-9-digit garbage, keep alphanumeric codes) from BBNY-only to every source format — header-based exports (csv-headers, xlsx-headers) had the same zip+4/leading-zero issues and were previously left uncleaned |
| 2026-08-05 | Added a second Country Code default: when Country Code and State are both blank and Zip Code is a plain 5-digit number, default to US (skipped for BBNY, which keeps Country Code blank by explicit decision) |
