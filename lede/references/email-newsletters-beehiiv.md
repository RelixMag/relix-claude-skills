# Lede_Docs - Email-Newsletters-Beehiiv

**Pages:** 10

---

## What Are Newsletters?

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/what-are-newsletters/

**Contents:**
- What Are Newsletters?
- Overview
- Key Properties of a Newsletter
- Managing Newsletters
- How Subscriber Preferences Are Tracked

In the Lede platform, a newsletter represents a recurring email publication that subscribers can opt into. Each publisher can have one or more newsletters. Newsletters are the core unit around which email subscriptions, opt-in preferences, and sending are organized.

Every publisher has a default newsletter, which new subscribers are automatically opted into when they register or begin a paid subscription. Publishers may also create additional newsletters for different topics, formats, or audiences.

Newsletters are created and managed through the Publisher App . From its Newsletters section, you can:

When a newsletter is created or updated in the Publisher App, the platform automatically provisions the corresponding resources in Beehiiv, including creating the custom fields needed to track subscriber preferences. See How Newsletters Are Represented in Beehiiv for details on this mapping.

The Lede platform stores each subscriber’s newsletter preferences in its database, recording which newsletters they are currently opted into and which they have opted out of. When a subscriber opts into or out of a newsletter — whether through your website, the Beehiiv preferences page, or by other means — their preference is updated in the database and the change is synced to Beehiiv automatically.

Was this article helpful?

Thanks for the feedback!

---

## Triggering Beehiiv Automations for New and Upgrading Subscribers

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/triggering-beehiiv-automations-for-new-and-upgrading-subscribers/

**Contents:**
- Triggering Beehiiv Automations for New and Upgrading Subscribers
- Overview
- Prerequisite: Add an “Add by API” trigger to your automation
- Assigning automations in the Publisher App
  - Beehiiv Settings
  - Non-paying Subscribers
  - Newsletters and welcome automation by product purchase
- Alternative: Trigger Automations from a Segment
- Choosing the right approach
- Tips

A Beehiiv automation is a sequence of one or more emails that Beehiiv sends to a subscriber in response to a certain condition. Automations are most commonly used for welcoming someone who has just registered for a free account or just purchased a paid subscription.

Subscribers on the Lede platform are pushed to Beehiiv via the Beehiiv API rather than through a Beehiiv-hosted signup form. Two quirks of the Beehiiv API affect which automations fire automatically:

To make sure the right people receive the right welcome emails, Lede lets you assign Beehiiv automations directly from the Publisher App — separately for non-paying registrations and for each paid product purchase. Lede then enrolls the subscriber in the assigned automation at the moment they register or complete a purchase, so the email fires at the right time regardless of how Beehiiv’s own triggers behave.

Before an automation can be assigned in the Publisher App, it must have an active “Add by API” trigger in Beehiiv. Without it, Beehiiv rejects API enrollment requests and the automation will not fire.

Lede only lists automations that have an active “Add by API” trigger. If you don’t see your automation in the dropdowns described below, double-check this trigger in Beehiiv.

Open the Publisher App and go to Settings → Newsletter Options. The page is organized into three groups:

Displays the read-only Publication ID that Lede syncs subscribers to. If you ever need this changed, contact Lede support.

Controls what happens when someone registers for a free account on your site (no purchase).

For each active product (subscription, gift, donation, etc.), you can configure:

You can use different automations for different products — for example, a “welcome to the membership” series for your annual subscription and a separate “thank you for your gift” series for gift purchases.

Click Save Settings to apply your changes.

If you’d rather build automations around newsletter subscriptions or other subscriber attributes — for example, a tailored welcome series for each newsletter — you can use Beehiiv’s “Added to segment” trigger instead of (or in addition to) the automations assigned in the Publisher App.

Lede maintains a Beehiiv custom field for each of your newsletters and updates it whenever a subscriber opts in or out. You can build a Beehiiv segment that captures subscribers of a given newsletter, or subscribers at a particular paid tier, and then run an automation any time a contact joins that segment.

When a Lede subscriber opts into that newsletter — at registration, when purchasing a product, or by toggling their preferences in their account — Lede updates the corresponding Beehiiv custom field. Beehiiv recalculates segment membership, the subscriber is added to the segment, and the automation fires.

Was this article helpful?

Thanks for the feedback!

---

## Newsletter Opt-In and Opt-Out

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/newsletter-opt-in-and-opt-out/

**Contents:**
- Newsletter Opt-In and Opt-Out
- Overview
- How Opt-In and Opt-Out Work
- Where Can Subscribers Change Their Preferences?
  - Through Your Website
  - Through Beehiiv’s Preferences Page
- Default Newsletter Opt-In
- Premium Newsletter Auto-Enrollment

When a subscriber opts into or out of a newsletter, the change is recorded in both the Lede platform and Beehiiv. This article explains how the opt-in/opt-out process works and how data stays in sync across both systems.

Each subscriber’s preference for each newsletter is tracked as an intent — a record that links the subscriber to a specific newsletter and stores whether they are active (opted in) or inactive (opted out).

When a subscriber’s preference changes, the platform immediately syncs the updated value to Beehiiv by setting the corresponding boolean custom field:

Subscribers can opt in or out of newsletters in several ways:

Your Lede-powered website includes newsletter preference controls where logged-in subscribers can manage which newsletters they receive. Changes made here are synced to Beehiiv automatically.

Beehiiv provides a built-in subscriber preferences page where subscribers can manage their email preferences. If a subscriber changes their newsletter selections through this page, the change is sent back to Lede via webhook (and also reconciled at the subscriber’s next login). See Subscriber Preferences and Unsubscribe Requests for details on how to configure which newsletters appear on this page.

When a new subscriber registers or purchases a paid subscription, they are automatically opted into your publication’s default newsletter. This happens whether the subscriber registers through your website, through a Stripe checkout flow, or through any other supported registration method.

Newsletters marked as premium are automatically enabled for subscribers when they purchase a paid subscription that includes the premium newsletter entitlement. Paid subscribers do not need to manually opt in to premium newsletters — it happens automatically when their subscription is created.

Was this article helpful?

Thanks for the feedback!

---

## Creating a New Newsletter

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/creating-a-new-newsletter/

**Contents:**
- Creating a New Newsletter
- Overview
- Step-by-Step: Creating a Newsletter
- After Creating a Newsletter
  - Create a Segment in Beehiiv
  - Enable on the Preferences Page
  - Set as Default (Optional)
- Editing a Newsletter

This article walks you through creating a new newsletter in the Publisher App. When you create a newsletter, the Lede platform automatically sets up the corresponding custom field in Beehiiv so that subscriber preferences are tracked and synced.

After saving, the platform will automatically create the corresponding Newsletter: [Display Name] custom field in your Beehiiv publication.

Once your newsletter is created, there are a few additional steps to consider:

To send emails to subscribers of this newsletter, you will need to create a segment in Beehiiv that filters by the new custom field. See Sending to Newsletters: Segments in Beehiiv for instructions.

If you want subscribers to be able to opt in or out of this newsletter through Beehiiv’s built-in preferences page, you will need to configure the custom field to be visible there. See Subscriber Preferences and Unsubscribe Requests for details.

If this should be the newsletter that new subscribers are automatically opted into upon registration, contact Lede support to set it as your publication’s default newsletter.

To edit an existing newsletter, click on it in the Newsletter list view. You can update any of the fields described above. Note that if you change the Display Name, the corresponding custom field in Beehiiv will be updated to match the new name.

Was this article helpful?

Thanks for the feedback!

---

## Customer Sync Between Lede and Beehiiv

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/customer-sync-between-lede-and-beehiiv/

**Contents:**
- Customer Sync Between Lede and Beehiiv
- Overview
- When Are Subscribers Synced to Beehiiv?
  - 1. New Subscriber Registration
  - 2. Email Verification
  - 3. Newsletter Opt-In or Opt-Out
  - 4. Subscription Changes
  - 5. Subscriber Login
- Reverse Sync: Beehiiv to Lede
  - Webhooks

The Lede platform automatically keeps subscriber data in sync with Beehiiv. This sync is bidirectional: changes made through your website or the Publisher App are pushed to Beehiiv, and changes made in Beehiiv (such as through subscriber preferences) are pulled back into Lede. This article explains when and how this sync occurs.

Subscriber data is synced from Lede to Beehiiv in the following situations:

When a new subscriber registers on your site and verifies their email address, they are automatically synced to Beehiiv. As part of this process:

If a subscriber was created but has not yet verified their email, the sync is triggered when they complete verification. Unverified subscribers are not synced to Beehiiv.

Whenever a subscriber opts into or out of a newsletter on your site, the change is immediately synced to Beehiiv by updating the corresponding boolean custom field.

When a subscriber purchases, upgrades, renews, or cancels a paid subscription, the platform syncs updated custom fields (such as product name, billing interval, and expiration date) and updates the subscriber’s Beehiiv tier. See Paid Subscriptions and Beehiiv Tiers for more details.

Each time a subscriber logs in, the platform updates their last_login and ever_logged_in custom fields in Beehiiv. Additionally, the login event triggers a reverse sync that pulls the subscriber’s current preferences from Beehiiv back into Lede. This ensures that any changes the subscriber made directly through Beehiiv’s preferences page are reflected on your site.

Changes made in Beehiiv are synced back to Lede through two mechanisms:

Beehiiv sends automatic notifications to the Lede platform whenever a subscription is created or updated. Lede processes these events and updates the subscriber’s newsletter preferences to match. For example, if a subscriber opts out of a newsletter via Beehiiv’s preferences page, the notification triggers Lede to mark that newsletter as inactive for the subscriber.

When a subscriber logs into your site, the platform fetches their current custom field values from Beehiiv and reconciles any differences. This acts as a safety net to catch any changes that may not have been captured by webhooks.

Was this article helpful?

Thanks for the feedback!

---

## Beehiiv Administration, Billing, and Support

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/beehiiv-administration-billing-and-support/

**Contents:**
- Beehiiv Administration, Billing, and Support
- Overview
- Onboarding
- Billing
- Accessing Beehiiv
- Getting Help

Beehiiv is set up and managed as part of your Lede platform. This article covers how Beehiiv is provisioned, how billing works, and how to get help with Beehiiv-related issues.

Beehiiv is provisioned for your publication as part of the Lede onboarding process. During onboarding, the Lede team will:

You do not need to create a Beehiiv account yourself — this is handled entirely by the Lede team as part of your platform setup.

Beehiiv usage is included in your Lede invoice. You do not receive a separate bill from Beehiiv, and you do not need to manage Beehiiv billing or payment methods independently. The cost is based on your active subscriber count and is incorporated into your regular Lede platform charges.

Notably, there is no limit on the number of emails you can send through Beehiiv. Unlike some email platforms that charge per email or impose monthly send limits, your Beehiiv plan through Lede allows unlimited sends. You can send as many newsletters, campaigns, and automated emails as you need without worrying about overage charges.

While newsletter management (creating newsletters, managing subscriber preferences) is handled through the Publisher App, you will use the Beehiiv dashboard directly for tasks such as:

Your Lede team will provide you with access credentials to the Beehiiv dashboard during onboarding.

If you experience any issues with Beehiiv — whether related to email delivery, subscriber sync, segments, analytics, or any other aspect of the integration — please contact Lede support first. Our support team is trained on the Beehiiv integration and can diagnose and resolve most issues directly.

If an issue requires deeper investigation, the Lede team can escalate to specialized Beehiiv support on your behalf. This ensures that Beehiiv’s support team has the full context of your Lede integration when troubleshooting.

Please do not file general support requests directly with Beehiiv. Because your Beehiiv publication is managed as part of the Lede platform, Beehiiv’s general support team may not have the context needed to assist you effectively, and direct requests may conflict with the way your account is configured. Routing all support through Lede ensures the fastest and most accurate resolution.

Was this article helpful?

Thanks for the feedback!

---

## Paid Subscriptions and Beehiiv Tiers

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/paid-subscriptions-and-beehiiv-tiers/

**Contents:**
- Paid Subscriptions and Beehiiv Tiers
- Overview
- How Tiers Work
- How Tier Assignment Works
- Premium Newsletters
- Using Tiers in Beehiiv

Beehiiv has a built-in concept of subscriber tiers that distinguishes between free and paid subscribers. The Lede platform uses this tier system to automatically reflect a subscriber’s paid subscription status in Beehiiv. This article explains how tiers work and how they are managed.

Every subscriber in Beehiiv is assigned to a tier:

Custom tiers are set up in Beehiiv when your publication is first onboarded, and new tiers are created automatically whenever you add a new product in the Publisher App.

A subscriber’s tier is determined automatically based on their active subscriptions:

Tier assignment is updated whenever:

Tiers also control access to premium newsletters. When a newsletter is marked as premium in the Publisher App, subscribers with an active paid subscription that includes the premium newsletter entitlement are automatically opted in. If a subscriber’s subscription lapses, their premium newsletter preferences are retained, but they can be targeted separately using segments (see Sending to Newsletters: Segments in Beehiiv).

Tiers can be used in Beehiiv to:

For example, you could create a segment for “All subscribers in the Premium Digital tier” to send an exclusive newsletter edition, or target “Free tier” subscribers with an upgrade offer.

Was this article helpful?

Thanks for the feedback!

---

## Sending to Newsletters: Segments in Beehiiv

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/sending-to-newsletters-segments-in-beehiiv/

**Contents:**
- Sending to Newsletters: Segments in Beehiiv
- Overview
- Why Segments Are Needed
- Creating a Segment for a Newsletter
- Combining Filters
  - Paid Subscribers of a Specific Newsletter
  - Free Subscribers Only
  - Active Subscribers Who Have Logged In
- Tips

When you are ready to send an email to subscribers of a specific newsletter, you need to create a segment in Beehiiv that targets the right audience. Because the Lede platform supports multiple newsletters per publisher, and subscriber preferences are tracked via custom fields, segments are the mechanism you use to direct your email sends to the correct recipients.

In Beehiiv, all of your subscribers exist in a single subscriber list. Unlike some email platforms that use separate lists for each newsletter, the Lede integration uses custom field values to track which newsletters each subscriber is opted into. Segments allow you to filter this single list down to exactly the subscribers you want to reach.

To send to subscribers of a specific newsletter, create a segment in Beehiiv with the following filter:

When composing an email, select this segment as your audience to send only to subscribers who have opted into that newsletter.

You can combine multiple filter conditions to create more targeted segments. Some useful examples:

Filter by both the newsletter custom field and the subscriber’s tier:

Target free subscribers for upgrade messaging:

Use the ever_logged_in or last_login custom fields to target engaged subscribers:

Was this article helpful?

Thanks for the feedback!

---

## How Newsletters Are Represented in Beehiiv

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/how-newsletters-are-represented-in-beehiiv/

**Contents:**
- How Newsletters Are Represented in Beehiiv
- Overview
- Custom Fields for Newsletters
- Other Custom Fields
- How Field Matching Works

Beehiiv is the email service provider that powers newsletter delivery for the Lede platform. Each newsletter that you manage in the Publisher App is represented in Beehiiv as a custom field on each subscriber’s profile. This article explains how that mapping works.

For each newsletter you create in the Publisher App, a corresponding boolean custom field is automatically created in your Beehiiv publication. The field follows this naming convention:

Newsletter: [Display Name]

For example, if you have a newsletter with the display name “Daily Briefing,” the custom field in Beehiiv will be named Newsletter: Daily Briefing.

The value of this field is a simple true or false:

These fields are created automatically when your publication is first set up in Beehiiv, and whenever you add a new newsletter through the Publisher App.

In addition to newsletter subscription fields, the Lede platform also syncs a number of other subscriber data points to Beehiiv as custom fields. These include:

These fields are useful for building segments in Beehiiv to target specific subscriber groups. See Sending to Newsletters: Segments in Beehiiv for more details.

When the Lede platform syncs data to and from Beehiiv, field names are matched in a case-insensitive manner. This means that “Newsletter: Daily Briefing” and “newsletter: daily briefing” are treated as the same field. This prevents accidental duplication if field names vary slightly in capitalization.

Was this article helpful?

Thanks for the feedback!

---

## Email Newsletters

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/

**Contents:**
- Email Newsletters
  - Beehiiv Administration, Billing, and Support
  - Creating a New Newsletter
  - Customer Sync Between Lede and Beehiiv
  - How Newsletters Are Represented in Beehiiv
  - Newsletter Opt-In and Opt-Out
  - Paid Subscriptions and Beehiiv Tiers
  - Sending to Newsletters: Segments in Beehiiv
  - Subscriber Preferences and Unsubscribe Requests
  - Triggering Beehiiv Automations for New and Upgrading Subscribers

Was this article helpful?

Thanks for the feedback!

---
