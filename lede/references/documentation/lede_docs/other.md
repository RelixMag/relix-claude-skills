# Lede_Docs - Other

**Pages:** 14

---

## Accessing the Lede WordPress Admin Dashboard

**URL:** https://docs.joinlede.com/getting-started/accessing-the-lede-wordpress-admin-dashboard/

**Contents:**
- Accessing the Lede WordPress Admin Dashboard
- Getting Initial Access to the Lede WordPress Admin:
- Resetting Your Password

If you forget your password:

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
The Lede team or a WordPress Admin on your team need to add you to WordPress if you don’t have access already.
```

---

## End User Account Deletion

**URL:** https://docs.joinlede.com/end-user-faqs-and-how-tos/end-user-account-deletion/

**Contents:**
- End User Account Deletion

Users cannot delete their account via their My Account page. If you have a user who wants their account deleted, please contact the Lede team to have their account removed.

Deleting a user via Stripe, SendGrid, or Beehiiv will not remove the user from the Lede CDP. Contact Lede before deleting users from those platforms to ensure that data remains properly synced.

Please keep in mind that if the user was previously a paying subscriber, information related to their payments and transactions will not be deleted.

Was this article helpful?

Thanks for the feedback!

---

## Payments & Billing

**URL:** https://docs.joinlede.com/stripe-related/

**Contents:**
- Payments & Billing
  - How to Use Stripe as a Lede Publisher
  - Stripe Automatic Tax Calculation
  - Stripe Settings Overview

Was this article helpful?

Thanks for the feedback!

---

## Hello world!

**URL:** https://docs.joinlede.com/hello-world/

**Contents:**
- Hello world!

Welcome to Lede Network. This is your first post. Edit or delete it, then start blogging!

---

## Connecting AI Tools

**URL:** https://docs.joinlede.com/connecting-ai-tools/

**Contents:**
- Connecting AI Tools
- What you can ask
- What it can and cannot do
- Connecting
  - Claude web or desktop app
  - Claude Code
- Who can connect
- What the assistant can see
- Limits worth knowing
- Privacy and security

Lede runs a connector that lets an AI assistant read your publication’s analytics data and answer questions about it in plain English. Instead of picking a report and setting a date range, you can ask “which articles brought in the most new subscribers last month?” and the assistant works out the query itself.

It uses the Model Context Protocol (MCP), an open standard for connecting AI assistants to outside data. Any tool that supports MCP can connect — Claude’s web app, desktop app and command-line tool all do.

The connector reaches the same warehouse behind the Analytics tab, but without the fixed set of reports. Questions that work well:

You can also ask follow-up questions, ask it to show the query it ran, and ask it to chart or summarise the result — whatever your AI tool is capable of.

The connector is strictly read-only. It cannot create, change or delete anything — not customers, subscriptions, products, coupons, settings or content. That restriction is enforced by the database itself, not just by convention, so no phrasing of a request can talk it into making a change.

It can read your analytics and commerce data: the event stream (page views, clicks, gate views, sign-ups, purchases, cancellations) and the supporting records for customers, products, orders, payments, sales, coupons and newsletters. It is scoped to your own publication and cannot see another publisher’s data.

The server address is:

There is no API key and no token to copy. You sign in with the same Lede account you use for the Publisher App, in your browser. If any tool asks you to paste a Lede API key, something is wrong — stop and contact support.

The connector is now live. Start a new conversation and ask a question about your data.

Or add it to your MCP configuration file directly:

The same browser sign-in and approval steps follow.

Anyone who can sign in to the Publisher App can connect, using that same account. There is nothing extra to request and no separate credential to generate.

The connector sees exactly the publications your account covers. If you look after several titles, one connection covers all of them — you name the publication you mean when you ask a question, and the assistant can switch between them.

Lede staff accounts must have two-factor authentication turned on before they can connect an AI tool. Publisher accounts can connect either way, though we recommend turning it on. You can do that under Profile in the Publisher App.

The connector offers the assistant five capabilities, all read-only:

You do not need to know any of this to use it. The assistant is briefed automatically on the shape of the data the moment it connects — including which figures are stored in cents rather than dollars, and how subscriptions link to payments — so plain-English questions generally work first time. If an answer looks wrong, asking it to show the query it ran is the quickest way to spot the problem.

Your data includes customer names and email addresses. Anything the assistant reads in order to answer you is sent to whichever AI provider you have connected. Treat this as you would any other tool you put customer data into, and check it sits within your own privacy policy and your obligations to subscribers. Asking for aggregate figures rather than lists of individuals is good practice.

For anything else, open a support ticket from the Support tab in the Publisher App.

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (yaml):
```yaml
https://app.joinlede.com/mcp
```

Example 2 (unknown):
```unknown
claude mcp add --transport http lede https://app.joinlede.com/mcp
```

Example 3 (json):
```json
{
  "mcpServers": {
    "lede": {
      "type": "http",
      "url": "https://app.joinlede.com/mcp"
    }
  }
}
```

---

## General Data Protection Regulation (GDPR) Compliance

**URL:** https://docs.joinlede.com/getting-started/general-data-protection-regulation-gdpr-compliance/

**Contents:**
- General Data Protection Regulation (GDPR) Compliance
- Action Required
- FYIs

All sites on the Lede network display a cookie consent modal to users who visit your site from a location governed by GDPR/CCPA. Users can “Accept all” or “Reject all” cookies and registered users can adjust these settings more granularly on their My Account page. The modal links out to your Privacy Policy, so please ensure this is up to date on your site.

You must designate your Privacy Policy page to ensure the proper link displays for your users in the modal. This has already been configured for all publishers on the platform as of 6/28/23 if you had an existing Privacy Policy/Notice page.

To designate your Privacy Policy page:

Navigate to the WordPress Admin > Settings > Privacy > Select your privacy policy page from the dropdown > click Use This Page

Users in the U.S. will not see this modal, unless they are located in California.

Users who make no selection or who reject cookies will not be included in your analytics data.

Was this article helpful?

Thanks for the feedback!

---

## Troubleshooting Common Login & Subscription Issues

**URL:** https://docs.joinlede.com/getting-started/troubleshooting-common-login-subscription-issues/

**Contents:**
- Troubleshooting Common Login & Subscription Issues

If any of your users are experiencing trouble with logging in or with their subscription benefits, please have them try the following troubleshooting actions based upon some common scenarios described below. Consider adding this information directly to your site so your users can attempt to help themselves when they run into these common issues.

I cannot log into the site.

I can log in to the site but the paywall is appearing even though I’m subscribed.

I am a paying subscriber but I cannot comment on articles.

I forgot my password.

Users can update their password by following these steps:

I cannot delete my saved credit card.

If you have an active subscription, it is not possible to delete the credit card you have on file. Please note that all payment information is stored securely in Stripe.

I cannot cancel my account.

If you have attempted to cancel your account, but the cancellation is not being processed, please contact Publisher Support (Publishers: add your support email here!).

I cannot delete my account.

This is a current limitation of the platform. If you wish to delete your account entirely, please contact Publisher Support (Publishers: add your support email here!). Please note that if you were previously a paying subscriber, information related to your payments & transactions will not be deleted and remains securely stored in Stripe.

If login/access issues persist after trying all of the above, please ask the user for more information.

Was this article helpful?

Thanks for the feedback!

---

## Lede Documentation

**URL:** https://docs.joinlede.com/author/ops874/

**Contents:**
- Lede Documentation
  - Analytics
  - Audience & Revenue
  - Connecting AI Tools
  - Creating Content
  - Email Newsletters
  - End-User FAQs
  - Getting Started
  - Integrations
  - Payments & Billing

Guides and answers for publishing on Lede.

First-party audience, conversion and revenue analytics in the Publisher App

Paywalls, promotions, gifts, and other revenue tools

Connect Claude or another AI assistant to your publication data and ask questions in plain English

Building posts and pages with blocks, images, and embeds

Creating and managing newsletters with Beehiiv

Ready-made help articles to share with your readers

Accounts, access, and the basics of your Lede site

Connecting third-party services like Coral and Google Ad Manager

Payment processing, taxes, and billing through Stripe

Managing customers, settings, and analytics in one place

Menus, homepages, branding, SEO, and sitewide settings

---

## Sample Page

**URL:** https://docs.joinlede.com/sample-page/

**Contents:**
- Sample Page

This is an example page. It’s different from a blog post because it will stay in one place and will show up in your site navigation (in most themes). Most people start with an About page that introduces them to potential site visitors. It might say something like this:

Hi there! I’m a bike messenger by day, aspiring actor by night, and this is my website. I live in Los Angeles, have a great dog named Jack, and I like piña coladas. (And gettin’ caught in the rain.)

…or something like this:

The XYZ Doohickey Company was founded in 1971, and has been providing quality doohickeys to the public ever since. Located in Gotham City, XYZ employs over 2,000 people and does all kinds of awesome things for the Gotham community.

As a new WordPress user, you should go to your dashboard to delete this page and create new pages for your content. Have fun!

---

## Lede Documentation

**URL:** https://docs.joinlede.com/

**Contents:**
- Lede Documentation
  - Analytics
  - Audience & Revenue
  - Connecting AI Tools
  - Creating Content
  - Email Newsletters
  - End-User FAQs
  - Getting Started
  - Integrations
  - Payments & Billing

Guides and answers for publishing on Lede.

First-party audience, conversion and revenue analytics in the Publisher App

Paywalls, promotions, gifts, and other revenue tools

Connect Claude or another AI assistant to your publication data and ask questions in plain English

Building posts and pages with blocks, images, and embeds

Creating and managing newsletters with Beehiiv

Ready-made help articles to share with your readers

Accounts, access, and the basics of your Lede site

Connecting third-party services like Coral and Google Ad Manager

Payment processing, taxes, and billing through Stripe

Managing customers, settings, and analytics in one place

Menus, homepages, branding, SEO, and sitewide settings

---

## End User FAQs

**URL:** https://docs.joinlede.com/end-user-faqs-and-how-tos/end-user-faqs/

**Contents:**
- End User FAQs
- Overview
- I’m an existing user. How do I log in to the site?
- I’m an existing user. How do I update my account details, including setting a password?

Lede publishers can copy and paste these FAQ’s for customers on to your site. Feel free to replace the language and screenshots to match your site’s branding or style.

Was this article helpful?

Thanks for the feedback!

---

## End-User FAQs

**URL:** https://docs.joinlede.com/end-user-faqs-and-how-tos/

**Contents:**
- End-User FAQs
  - Dark Mode FAQ for Your End Users
  - End User Account Deletion
  - End User FAQs

Was this article helpful?

Thanks for the feedback!

---

## Getting Started

**URL:** https://docs.joinlede.com/getting-started/

**Contents:**
- Getting Started
  - Accessing the Lede WordPress Admin Dashboard
  - General Data Protection Regulation (GDPR) Compliance
  - How to Enable Two-Factor Authentication for WordPress Admin
  - Troubleshooting Common Login & Subscription Issues

Was this article helpful?

Thanks for the feedback!

---

## Hello world!

**URL:** https://docs.joinlede.com/category/uncategorized/

**Contents:**
- Hello world!

Welcome to Lede Network. This is your first post. Edit or delete it, then start blogging!

---
