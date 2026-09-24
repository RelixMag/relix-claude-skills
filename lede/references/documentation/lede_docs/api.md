# Lede_Docs - Api

**Pages:** 1

---

## Subscriber Preferences and Unsubscribe Requests

**URL:** https://docs.joinlede.com/email-newsletters-beehiiv/subscriber-preferences-and-unsubscribe-requests/

**Contents:**
- Subscriber Preferences and Unsubscribe Requests
- Overview
- Beehiiv’s Subscriber Preferences Page
- Surfacing Individual Newsletters on the Preferences Page
- Newsletter-Level Opt-Out vs. Platform-Level Unsubscribe
  - Newsletter-Level Opt-Out
  - Platform-Level Unsubscribe
- Best Practices

Beehiiv provides a built-in subscriber preferences page that allows subscribers to manage their email settings. This article explains how to configure which newsletters appear on the preferences page, and the important distinction between newsletter-level opt-outs and a full platform-level unsubscribe.

Every Beehiiv publication has a preferences page that subscribers can access (typically via a link in the footer of your emails). This page allows subscribers to view and change their email preferences without needing to log into your website.

By default, the newsletter custom fields synced from Lede are not automatically displayed on Beehiiv’s preferences page. To allow subscribers to opt in or out of individual newsletters through the preferences page, you need to configure the relevant custom fields to be visible:

Once enabled, subscribers will see toggles for each newsletter on their preferences page, allowing them to opt in or out individually.

It is important to understand the difference between these two actions:

When a subscriber turns off a specific newsletter on the preferences page (or through your website), they are opting out of that individual newsletter only. Their Beehiiv subscription remains active, and they continue to receive any other newsletters they are still opted into. The corresponding custom field in Beehiiv is set to false, and the change is synced back to Lede.

Beehiiv also provides a full unsubscribe option, typically available at the bottom of emails and on the preferences page. When a subscriber uses this option, they are unsubscribing from all emails from your Beehiiv publication entirely. This is a different action from opting out of individual newsletters — it tells Beehiiv to stop sending all emails to that address.

A platform-level unsubscribe in Beehiiv does not cancel the subscriber’s account or paid subscription on your Lede site. It only affects email delivery. The subscriber’s account, subscription status, and content access on your website remain unchanged.

Was this article helpful?

Thanks for the feedback!

---
