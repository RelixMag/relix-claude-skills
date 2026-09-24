# Lede_Docs - Integrations-Coral-Gam

**Pages:** 8

---

## How to enable the Meta Pixel (formerly Facebook Pixel)

**URL:** https://docs.joinlede.com/integrations-coral-gam/how-to-enable-the-meta-pixel-formerly-facebook-pixel/

**Contents:**
- How to enable the Meta Pixel (formerly Facebook Pixel)

The Meta Pixel (formerly Facebook Pixel) is an analytics tool that tracks user actions on your website to help you understand how people interact with your site after viewing Facebook / Instagram ads.

The Meta Pixel integration on Lede, like all of our integrations, is optional. If you do not add a Pixel ID, the pixel will not be added to your site.

To implement the Pixel on your site, you will need a valid Meta Pixel ID. See the section below on How to Get a Meta Pixel ID.

Once you have a Pixel ID, open the Publisher App and go to Settings > Analytics & Tracking. Add your ID to the “Meta Pixel ID” field and click “Save”. The Pixel can take up to 30 minutes to load on your site.

The Lede implementation of the Meta Pixel includes 5 events. For details on these events, see the table below.

How to get a Meta Pixel ID

Getting a Meta Pixel ID involves accessing Meta’s Business tools. Here’s how to do it:

Meta Pixel Event Details

Was this article helpful?

Thanks for the feedback!

---

## Integrations

**URL:** https://docs.joinlede.com/integrations-coral-gam/

**Contents:**
- Integrations
  - Bluesky Integration for Author Profile
  - GAM: Automatically Insert In-Article Ads
  - Google AdWords & Conversion Tracking
  - How to Configure Commenting with Coral
  - How to Enable Google SSO for Your Users
  - How to enable the Meta Pixel (formerly Facebook Pixel)
  - How to Setup Google Ad Manager (GAM) – Lede-Assisted
  - How to Setup Google Ad Manager (GAM) – Self-Serve

Was this article helpful?

Thanks for the feedback!

---

## GAM: Automatically Insert In-Article Ads

**URL:** https://docs.joinlede.com/integrations-coral-gam/gam-automatically-insert-in-article-ads/

**Contents:**
- GAM: Automatically Insert In-Article Ads
- How to automatically insert in-article ads
- Things to keep in mind

If you have Google Ad Manager (GAM) setup on your site, you can configure how in-article ads (300×250) are automatically inserted into the posts on your site.

Was this article helpful?

Thanks for the feedback!

---

## How to Setup Google Ad Manager (GAM) – Lede-Assisted

**URL:** https://docs.joinlede.com/integrations-coral-gam/how-to-setup-google-ad-manager-gam-lede-assisted/

**Contents:**
- How to Setup Google Ad Manager (GAM) – Lede-Assisted
- Google Ad Manager (GAM) Setup
- Ad Units
- Key-values
- Orders
- Ads on Lede

In addition to Sponsorships (currently referred to as “Ad Campaigns” in the WordPress Admin), Lede also currently supports three “Ad units” that can be served via Google Ad Manager (GAM). The Lede team can assist with your initial GAM setup to ensure Lede-compatible ad units and associated placements are created. Alternatively, you can set up everything yourself.

To allow the Lede team to assist with setup, invite analytics@joinlede.com as an Admin to your Google Ad Manager account, if you haven’t already done so.

The Lede platform currently supports three Ad Units:

Was this article helpful?

Thanks for the feedback!

---

## How to Enable Google SSO for Your Users

**URL:** https://docs.joinlede.com/integrations-coral-gam/how-to-enable-google-sso-for-your-users/

**Contents:**
- How to Enable Google SSO for Your Users
    - Example of Steps 3 and 4
    - Example of Steps 5 and 6

Following the transition of the Lede platform from a custom-built login system to AuthJS, Google SSO will be available to end-users. Google SSO is optional – users will be able to login with password or link sent to their email address. To enable Google SSO for your users, follow the instructions below:

Login to Google as your preferred account owner (we recommend an account associated with your domain, rather than a personal email)

Go to Google Cloud’s Create Client page

If prompted to, create a new project named anything you like (such as the name of your website), then create to the Create Client page.

Under “Application Type” select “Web application”

Select any name for the credential you’d like (this won’t be displayed publicly)

Under “Authorized JavaScript origins” add your site’s homepage address (e.g. “https://joinlede.com”)

Under “Authorized redirect URIs” add your site’s homepage address plus /api/auth/callback/google at the end (e.g. https://joinlede.com/api/auth/callback/google)

Copy the Client ID and Client Secret values

Enter your credentials

Was this article helpful?

Thanks for the feedback!

---

## How to Setup Google Ad Manager (GAM) – Self-Serve

**URL:** https://docs.joinlede.com/integrations-coral-gam/how-to-setup-google-ad-manager-gam-self-serve/

**Contents:**
- How to Setup Google Ad Manager (GAM) – Self-Serve
- Google Ad Manager (GAM) Setup
- Ad Units
- Placements
- Key-values
- Orders
- Lede Specific Setup

In addition to Sponsorships (currently referred to as “Ad Campaigns” in the WordPress Admin), Lede also currently supports three “Ad units” that can be served via Google Ad Manager. This article provides instructions for you to set up these ad units, placements, and key-values yourself. Alternatively, the Lede team can assist with your initial GAM setup to ensure Lede-compatible ad units and associated placements are created.

Log into your Google Ad Manager account.

For each ad unit, go to Inventory > Ad units > New ad unit:

Go to Inventory > Ad units > Placements > New placement:

Key-values are used to dynamically target ads based on your WordPress tags and categories.

For each key-value, go to Inventory > Key-values > New Key-value:

Once Google Ad Manager is set up, there is some minimal Lede set up.

Was this article helpful?

Thanks for the feedback!

---

## Bluesky Integration for Author Profile

**URL:** https://docs.joinlede.com/integrations-coral-gam/bluesky-integration-for-author-profile/

**Contents:**
- Bluesky Integration for Author Profile

We have implemented a Bluesky handle integration for author profiles. To incorporate your Bluesky presence:

Navigate to Profiles > All Profiles

Scroll to the Info section

Locate the Bluesky field (positioned beneath Twitter)

Enter your handle and select “Update”

Important note: Do not include https://bsky.app/profile/ – that segment of the link will be generated programmatically.

Your Bluesky handle will immediately appear on your author page, helping you connect with readers across platforms.

Was this article helpful?

Thanks for the feedback!

---

## Google AdWords & Conversion Tracking

**URL:** https://docs.joinlede.com/integrations-coral-gam/google-adwords-conversion-tracking/

**Contents:**
- Google AdWords & Conversion Tracking

If you are using Google AdWords, you can now add an associated conversion tag to your Lede platform site. A conversion tag tracks when someone who has clicked your ad goes to your website and completes a valuable action – in the case of the Lede platform, the conversion tag is used for tracking successful subscription purchases.

You first need to create a new conversion action in your Google AdWords account. Name the action something readable, like “purchase”.

Once you have your Google AdWords conversion tracking tag, complete the following steps to set this up on your Lede site:

Your conversion tracking tag has now been added to your site, and will track when a user who clicks on one of your ads successfully completes their subscription purchase and lands on the /payment/complete page.

Was this article helpful?

Thanks for the feedback!

---
