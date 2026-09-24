# Lede_Docs - Analytics

**Pages:** 5

---

## What is Beacon?

**URL:** https://docs.joinlede.com/analytics/what-is-beacon/

**Contents:**
- What is Beacon?
- Everything is an event
- How visitors and sessions are counted
  - Unique Users
  - Sessions
- What Beacon does not count
- How current the numbers are
- Why purchases are collected twice
- Where to find it

Beacon is Lede’s own analytics system. Every Lede publication collects its own audience data — page views, clicks, content gate impressions, sign-ups, purchases and cancellations — and stores it in a warehouse that only your publication can read. You read that data in the Analytics tab of the Publisher App.

Because Beacon is first-party, it is not blocked the way a third-party analytics tag often is, and it is joined directly to your customer records in Lede. The reader who saw three articles and hit a paywall is the same record as the person who subscribed a week later.

Beacon does not collect a fixed set of pre-computed reports. It records individual events, each stamped with the page, the article, the anonymous visitor, the session and the campaign it arrived from. Every report in the Analytics tab is a query over that event stream, which is why new questions can usually be answered without changing anything on your site.

The events collected today include:

Two identifiers do most of the work.

Lede stores a random anonymous ID in the reader’s browser. It lasts a year and is refreshed on every visit. Unique Users is the count of distinct IDs in the period you are looking at.

The visitor ID is stored per publication and per browser. A reader who visits two Lede publications is counted as a separate visitor on each one. Clearing site data, using private browsing, or switching browser or device also produces a new ID. Beacon does not stitch a person together across devices — the only durable person-level identity is a logged-in customer account.

A session is a single visit. It ends after 30 minutes of inactivity, and the next event starts a new one. Unlike Google Analytics, a Beacon session does not reset at midnight and does not restart when a reader arrives from a different campaign.

Unique Users and Sessions are approximate and not additive. Do not add up the daily Unique Users column to get a figure for the month: a reader who visited on three days appears in three daily rows but is one visitor for the month. Change the date range instead and let the report do the counting.

Beacon is not a real-time dashboard. Events are loaded into the warehouse in batches, and the Analytics tab caches each query for up to six hours on top of that. Expect the figures to be several hours behind, and treat the most recent day as incomplete. This is why the date filters default to ending yesterday rather than today.

All dates are UTC. A “day” in every report runs from 00:00 to 23:59 UTC, not from your newsroom’s local midnight. Keep that in mind when you line a Beacon figure up against a publishing time in your own timezone.

Roughly one in seven checkout events never reaches Beacon from the browser — readers close the tab as payment completes, or a privacy extension blocks the request. Lede’s payment system therefore reports every purchase a second time from the server.

The subscription and revenue reports read a merged, de-duplicated view of these two sources, so a purchase is counted exactly once no matter which route it arrived by. You do not need to do anything about it — it is worth knowing only because it explains why purchase counts in Beacon can be higher than what a browser-only analytics tool reports.

Beacon reports live in the Analytics tab of the Publisher App. See Accessing the Analytics tab for how to get there and how the controls work.

The standalone Beacon dashboard at app.ledebeacon.com has been retired. Everything it did is now in the Publisher App, alongside your customer, product and settings data.

Was this article helpful?

Thanks for the feedback!

---

## Analytics

**URL:** https://docs.joinlede.com/analytics/

**Contents:**
- Analytics
  - What is Beacon?
  - Accessing the Analytics tab
  - Traffic and content reports
  - Conversion, subscription and revenue reports

How Lede collects your audience data, and what the numbers do and do not mean

Where the Analytics tab lives, who can see it, and how the date, interval and series controls work

Overview, Traffic, Articles, Time, Referrers and Campaigns — what each one measures and how to read it

Conversion Events and Rates, Subscription Starts and Churn, and Recognised Revenue — and the caveats that matter

Was this article helpful?

Thanks for the feedback!

---

## Accessing the Analytics tab

**URL:** https://docs.joinlede.com/analytics/accessing-beacon/

**Contents:**
- Accessing the Analytics tab
- Getting there
- Who can see it
- Choosing a report
- Setting the date range and interval
- Reading a chart
- Reading a table
- What the Analytics tab does not do
- When a report looks empty

Beacon reports live in the Analytics tab of the Publisher App, alongside your customer, product and settings data.

If you used the standalone Beacon dashboard at app.ledebeacon.com, that site has been retired. Sign in to the Publisher App instead. Every report the old dashboard offered is here, plus subscription and revenue reporting it never had.

You land on the Overview, a seven-day summary. Every other report is one click away in the list on the left.

The screenshots in this guide come from the Lede FYI demo publication, so every figure in them is sample data.

Anyone who can sign in to your publication in the Publisher App can open the Analytics tab. There is no separate analytics permission to request and no extra role to assign.

Subscription Starts, Subscription Churn and Revenue appear only if your publication has at least one active product. If you do not sell subscriptions, you will see the eight traffic and conversion reports and nothing else — that is expected, not a fault.

The list on the left switches between reports. On a narrow screen or a phone it collapses into a single dropdown directly beneath the page heading.

The first six are covered in Traffic and content reports; the rest in Conversion, subscription and revenue reports.

Every report except the Overview has the same three controls.

The end date defaults to yesterday, not today, because the most recent day is always incomplete — see What is Beacon? for how far behind the data runs. If you set the end date to today, expect the last point on the chart to dip.

Your date range and interval are stored in the page address and carry over when you switch reports, so you can set the window once and click through every report. You can also bookmark or paste a link to a specific report and date range for a colleague.

Hourly over a long range produces thousands of points and a chart you cannot read. Use it for a few days at a time, and Weekly or Monthly for anything longer than a couple of months.

The coloured chips above each chart are both the legend and a filter. Click one to hide that series; click it again to bring it back. The chip fades and turns into an outline while the series is hidden.

If you switch every series off, the chart is replaced by Select a series to display. The colours stay attached to the same series as you toggle, so a line does not change colour when you hide its neighbour.

The chart trims empty periods from the start and end of the range, so a chart may begin later than your start date if nothing happened yet. The table below it always shows every row in the range.

Every report has a table under the chart with the same figures. Click a column heading to sort by it. Reports that rank things — articles, referrers, campaigns — chart the top 15 and list up to 250 rows in the table, so scroll the table if you want the long tail.

So you are not hunting for something that is not there:

If you need something the tab cannot do — an export, a custom breakdown, a one-off analysis — open a support ticket. Your publication’s data can be queried directly in the warehouse, and Lede can either run the query or arrange access for you.

Was this article helpful?

Thanks for the feedback!

---

## Conversion, subscription and revenue reports

**URL:** https://docs.joinlede.com/analytics/conversion-subscription-and-revenue-reports/

**Contents:**
- Conversion, subscription and revenue reports
- Conversion Events
- Conversion Rates
- Subscription Starts
- Subscription Churn
- Revenue

These five reports follow readers from hitting a content gate through to paying, cancelling and the revenue that results. The first two are available to everyone; the last three appear only if your publication has at least one active product. For the shared controls, see Accessing the Analytics tab.

The screenshots in this guide come from the Lede FYI demo publication, so every figure in them is sample data.

Up to four counts over time, the raw material of your registration and paywall funnel. Publications without an active product see the first three only.

These are event counts, not people. One reader who hits gates on four articles in an evening contributes four gate views. Gate views and dismissals are also counted once per time the gate is displayed, so a reader who scrolls back up to an article they already opened does not add a second one.

The gap between Gate Views and Gate Dismissals is the more useful shape here. A dismissal rate that climbs after you change your gate settings is a fast signal that the new configuration is landing badly.

Two series — Content Gate → Email Signup and Content Gate → Subscription — each expressing that outcome as a percentage of gate views in the same period. Publications without commerce see only the first.

This is a ratio, not attribution. It divides the sign-ups in a bucket by the gate views in that same bucket. It does not check whether the people who signed up were the same people who saw a gate, and it does not allow for someone seeing a gate on Monday and subscribing on Thursday. A reader who signs up from a newsletter link without ever seeing a gate still counts in the numerator.

The practical consequence is that the figure can exceed 100% when sign-ups are running ahead of gate impressions, and that a day with very few gate views will produce a wild-looking percentage. Read it as a trend line over a reasonable window rather than as a literal conversion rate, and switch to Weekly or Monthly if the daily line is too noisy to interpret.

If you need attribution — which article led to which signup or subscription — see the Email Signups and Subscriptions columns in the Articles report, which credit each conversion to the last article read in the same visit.

New subscriptions over time, split three ways.

This report reads the merged, de-duplicated record of each checkout, so a purchase is counted once whether it was reported by the reader’s browser or by our payment system. That is also why these figures can be higher than the purchase numbers a browser-only analytics tool shows you — roughly one in seven checkouts is never reported by the browser at all.

These are starts, not net growth. Renewals are not counted here, and neither are cancellations — pair this with Subscription Churn to see the whole picture.

Cancellations over time. All Products is the total; individual series are added for your most-cancelled products, up to twelve of them.

Churn counts the moment a reader chooses to cancel, not the moment their access ends. Someone who cancels an annual subscription in January but keeps reading until December appears on the January line. This report tells you when people decided to leave, which is what you want for spotting a bad week — but it is not a measure of subscribers lost in the period, and it will not reconcile against a billing report.

A subscription that lapses because a card failed, rather than because the reader cancelled, does not appear here. Neither does a cancellation that was later undone, which will still show as a cancellation on the day it happened.

If the report is empty, that is good news rather than a fault — it means no cancellations were recorded in the range.

Recognised revenue over time.

Recognised revenue spreads income across the period it covers rather than booking it all when the card is charged:

This is why a large annual sign-up does not produce a spike on the chart, and why revenue appears in months where nothing was actually charged. It gives you a smoother picture of the business than cash receipts do.

Two things to keep in mind. Refunds are not deducted — a refunded payment stays in the figures at its full value. And the report assumes a single currency and labels everything with a dollar sign, so if you sell in more than one currency the totals are not meaningful. For refund-adjusted or multi-currency figures, use your payment provider’s own reporting.

Renewals are included here, unlike in Subscription Starts. Revenue answers “what is the business worth this month”; Subscription Starts answers “how many new people joined”. They will not line up, and they are not supposed to.

Was this article helpful?

Thanks for the feedback!

---

## Traffic and content reports

**URL:** https://docs.joinlede.com/analytics/traffic-and-content-reports/

**Contents:**
- Traffic and content reports
- Overview
- Traffic
- Articles
- Time
- Referrers
- Campaigns

These six reports cover how many people came, what they read, how long they stayed and where they came from. They are available to every publication. For the controls shared by all of them, see Accessing the Analytics tab.

The screenshots in this guide come from the Lede FYI demo publication, so every figure in them is sample data.

The Overview is a fixed seven-day summary. It has no date controls — it always covers the last seven days.

The cards are simple event counts for the period:

Top Articles lists your five most-read articles over the same seven days, by page views. The title shown is the most recent one Beacon saw, so if you have re-headlined a piece you will see the new headline against all of its history. Signups and Subscriptions columns show how many email signups and paid subscriptions each article led to — see the Articles report for how those are attributed.

Median Time on Page shows a dash when there is no measured timing data. See the Time report below for why some page views are not measured.

Three series over the period you choose: Page Views, Sessions and Unique Users.

Sessions and Unique Users are approximate and cannot be added up across rows. If you want a monthly unique figure, set the date range to that month rather than summing the daily column. What is Beacon? explains why.

The ratio of page views to sessions is a decent loyalty signal: it tells you how many pages a typical visit covers. The ratio of sessions to unique users tells you how often people come back within the period.

Page views per article for the period, charted as a ranked bar chart of the top 15 and listed in full below it. Two further columns, Email Signups and Subscriptions, tie conversions back to your content: each conversion is credited to the last article the reader viewed in the same visit.

Articles are grouped by their internal ID, not by their headline, so you may see the same or a similar headline more than once in the table — those are genuinely different posts. Only pages Beacon could identify as a piece of content appear here; section fronts, the homepage and account pages are excluded.

Attribution is per visit, so the acquisition columns will not add up to the totals in the Conversion Events report — a reader who goes straight from an advert to your products page and subscribes never viewed an article, and that subscription is credited to no article at all. Read the columns as “conversions this article drove directly”.

How long readers actually spend on each article. This is the report to reach for when page views alone are not telling you which pieces landed.

Measured Views is always lower than Page Views. Timing depends on the reader’s browser sending a signal back while the page is open, and plenty of visits never do — a reader who opens a page and immediately leaves usually produces no timing at all. Articles with no measured views are left out of this report entirely. Read the percentages as “of the readers we could measure”, not “of everyone”.

The report uses the median rather than an average on purpose. A single tab left open overnight would drag an average into the hours; the median ignores it. Typical values sit in the 20 to 60 second range, so do not be alarmed by a number that looks low — compare articles against each other rather than against an absolute target.

Where your page views came from, based on the referring address the browser reported.

The Hide on-site referrers chip filters out readers arriving from your own site — someone clicking from one article to the next. Turn it on when you want external traffic sources only; leave it off to see internal navigation as well.

The Median Seconds column shows how long readers from each source stayed, which is often more revealing than the volume alone: a source sending fewer but far more engaged readers is worth knowing about.

Referrers are listed as raw addresses, not grouped into channels. There is no “Social” or “Search” roll-up, so Google, Google News and a Google image search appear as separate rows, and a link shortener shows as the shortener rather than the platform behind it. Direct traffic, and any browser that withholds the referrer, is simply absent rather than listed as “direct”.

Page views broken down by the utm_campaign tag on the address a reader arrived at.

If you tag your newsletter links, social posts or paid placements with UTM parameters, each campaign appears here with its page views and median time on page, ranked highest first. If you do not tag anything, the report is empty — as above.

A campaign is credited only to the specific page view whose address carried the tag. It does not follow the reader through the rest of their visit, so a campaign that brings someone in who then reads five more articles is credited with one page view, not six. Treat this as “how many entries did this campaign drive”, not as full campaign attribution.

Was this article helpful?

Thanks for the feedback!

---
