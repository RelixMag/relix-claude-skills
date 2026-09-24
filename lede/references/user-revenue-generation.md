# Lede_Docs - User-Revenue-Generation

**Pages:** 10

---

## Ad Blocker Detection

**URL:** https://docs.joinlede.com/user-revenue-generation/ad-blocker-detection/

**Contents:**
- Ad Blocker Detection
- Choosing a mode
  - Soft mode (dismissible banner)
  - Hard mode (content gate)
- Who does not see the prompts
- Configuring detection in the Publisher App
- Recommendations

Ad Blocker Detection can help you recover ad revenue by identifying readers who have ad blockers active and prompting them to disable the blocker, log in, or subscribe. You can choose between a gentle reminder or a full content gate, and all reader-facing copy is configurable in the Publisher App.

Two modes are available, and they can be used independently or together.

Soft mode displays a notification bar at the top of the page when an ad blocker is detected. Readers can close the banner, and the dismissal persists for the rest of their browsing session. The banner reappears in the next session if the blocker is still active.

The default banner copy reads: “It looks like you’re using an ad blocker. Ads help support our journalism. Please consider disabling your ad blocker.” You can replace this with their own message in the Publisher App.

Hard mode displays a full-page overlay that blocks access to the article until the reader disables their ad blocker. The overlay uses the title “Ad Blocker Detected” and a body message that you can customize.

The call-to-action adapts to the reader’s current state:

Hard mode is only available when soft mode is also enabled. If soft mode is turned off, hard mode is automatically disabled as well.

Several groups are deliberately excluded to avoid frustrating legitimate users or breaking key flows:

Settings live under Ads → Ad Blocker Detection, which is open by default. Four fields are available:

Start with soft mode to gauge how readers respond before introducing the content gate. If you enable hard mode, take time to write gate copy that matches your publication’s voice, since this is often a reader’s first prompt to subscribe. Review the default CTAs to confirm that your /products page is configured for the subscription and upgrade paths the gate links to.

Was this article helpful?

Thanks for the feedback!

---

## Audience & Revenue

**URL:** https://docs.joinlede.com/user-revenue-generation/

**Contents:**
- Audience & Revenue
  - Ad Blocker Detection
  - Ad Campaigns (Sponsorships)
  - Category-Specific Content Gate Overrides
  - Converting User Emails to Paying Subscribers
  - Gift Articles
  - Gift Subscriptions
  - How to Configure the Registration Walls and Paywalls
  - How to Use Promotional Pricing (including Coupon Codes)
  - Intro Pricing FAQs

Was this article helpful?

Thanks for the feedback!

---

## Ad Campaigns (Sponsorships)

**URL:** https://docs.joinlede.com/user-revenue-generation/ad-campaigns-sponsorships/

**Contents:**
- Ad Campaigns (Sponsorships)
- Campaign Display Fields
- Leaderboard Display Fields
- Targets
- Leaderboard Display with centered message
- Leaderboard Display with left-aligned message
- Article Banner Display

The Lede platform offers the ability to set ad campaigns on your website. This functionality can be used for sponsorships, subscription sale advertising, and other similar purposes. To access Ad Campaigns, navigate to your WordPress Admin and click the Ad Campaigns menu item.

See annotated screenshots at the bottom of this page for where fields display in all available targets. Please note that the Leaderboard has a separate module.

Select which targets you want your Ad Campaign to appear in:

Homepage Card Display

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
If you have multiple site-wide Ad Campaigns or multiple Ad Campaigns that have selected the same category that are all published, the most recently published Ad Campaign is the one that will display.
```

---

## Intro Pricing FAQs

**URL:** https://docs.joinlede.com/user-revenue-generation/intro-pricing-faqs/

**Contents:**
- Intro Pricing FAQs

This document helps explain Lede’s intro pricing model, which offers subscribers a low-cost trial month before transitioning to a standard annual subscription. Designed to lower acquisition barriers while establishing valuable long-term subscriber relationships, intro pricing can be an effective tool for converting interested readers into committed subscribers. Below you’ll find answers to common questions about how intro pricing works, eligibility requirements, cancellation policies, and how this promotion appears to your subscribers.

What distinguishes intro pricing from other kinds of sales or coupons?

Intro pricing offers a 1-month trial at a reduced rate that automatically converts to an annual subscription. The key distinction from other promotions is the interval switch from monthly to annual. While the monthly trial price is discounted, the subsequent annual subscription is at the standard rate.

Can existing monthly subscribers switch to intro pricing and then convert to annual?

No. Sales and promotions are not available to current subscribers, so existing monthly subscribers are not eligible for this promotion.

Could a user cancel before the trial ends, then re-subscribe with the same email address to repeatedly pay only the trial price?

When a user cancels, their subscription remains active until the end of their current billing period unless the publisher initiates an immediate cancellation in Stripe with a prorated refund.

Example with a regular subscription

Travis has a monthly subscription renewing on May 25. He cancels on May 12, but his subscription remains active until May 25. During this period, he can reverse his cancellation, but remains ineligible for promotions as he still has an active subscription. After May 25, he could sign up as a new subscriber and would be eligible for any current promotions.

Example with Intro Pricing

Taylor subscribes via intro pricing and cancels with two weeks remaining in her trial month. She remains an active subscriber for those two weeks and cannot access intro pricing again while her subscription is active. After her subscription expires, she would technically be eligible for intro pricing if the promotion is still available—however, most intro pricing promotions run for less than one month.

Can introductory pricing last longer than one month, such as a 3-month trial before converting to annual pricing?

No. The initial term for intro pricing is strictly limited to one month.

Do subscribers receive notification when their intro pricing period is ending and converting to the annual rate?

No automatic notification is sent. However, publishers have the option to send an email to all promotion participants as the intro period concludes.

Can intro pricing work with a monthly subscription—starting with a trial price before converting to the regular monthly rate?

No. A promotion where the subscription interval remains unchanged (monthly to monthly) is considered a standard sale, not intro pricing.

How is intro pricing displayed on the products page?

Intro pricing is clearly indicated on the product card with the original price struck through and the promotional offer displayed below. The message follows this format: “[Intro price] for the first month, then [annual price] per year.”

Example: For a $2 intro price leading to a $50 annual subscription, the display would read: “$2 for the first month, then $50 per year.”

How is intro pricing information shown on the user’s account page?

The subscription tab on the user’s account page provides comprehensive subscription details, including the product name, renewal date, and payment method.

When a discount is applied, the Active Discount field appears with a description of the promotion.

For subscriptions with intro pricing, an additional field appears with the heading “After this date, your subscription will be” followed by the future subscription amount and term.

Example of Intro Pricing displayed on the user’s Account page

Was this article helpful?

Thanks for the feedback!

---

## Value Proposition

**URL:** https://docs.joinlede.com/user-revenue-generation/value-proposition/

**Contents:**
- Value Proposition
- Login Page
- Register Page
- Products Page
- Product Group Page

You can add text to your Login page, your Products page and your Product Group page (if applicable) to explain to prospective subscribers why they should consider subscribing to your site.

Text added to your Login page is added directly underneath the Login form and displays in a banner with a background color that stretches across the width of the page.

To add a value proposition to your Login page (located at /login):

Text added to your Register page is added directly underneath the Register form and displays in a banner with a background color that stretches across the width of the page (similar to Login Page).

To add a value proposition to your Register page (located at /register):

Text added to your Products page is added directly underneath your logo and displays in a banner with a background color that stretches across the width of the page.

To add a value proposition to your Products page (located at /products):

Text added to your Product Group page is added directly underneath your logo and displays in a banner with a background color that stretches across the width of the page.

If you have a Product Group offering, you can add a separate value proposition to this page. To add a value proposition to your Product Group page (located at /products/[product-group-name]):

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
For all pages, be mindful of how much text you are including and how it displays on both desktop and mobile. The purpose of these pages is to get users to complete the flow that they are in - a lot of text might have the opposite effect.
```

Example 2 (unknown):
```unknown
If you have an active site-wide Promotion running, or if you have checked "Force Promotion Message Display" for a Promotion description, the Value Proposition will NOT display on your Product related pages.
```

---

## How to Configure the Registration Walls and Paywalls

**URL:** https://docs.joinlede.com/user-revenue-generation/how-to-configure-the-registration-walls-and-paywalls/

**Contents:**
- How to Configure the Registration Walls and Paywalls
- Registration Wall Settings
- Paywall Settings

The available Registration Wall & Paywall settings have been expanded to allow additional configurability for when and how users are prompted to provide their email addresses and purchase a subscription. It is also possible to configure Category-specific Registration Wall & Paywall settings. It is currently not possible to configure the paywall on a per-article basis.

To review and adjust these settings, open the Publisher App and go to Settings > Registration Wall or Settings > Paywall.

The registration wall settings control when and how a user is prompted to provide their email address.

The paywall settings control when and how a user is prompted to purchase a subscription.

An article with a hard registration wall, where blocks to preview is set to 0 (zero).

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
The article allotment counter keeps track of which articles a user has read. Navigating to the same article twice will only count once against the allotment.
```

---

## Gift Subscriptions

**URL:** https://docs.joinlede.com/user-revenue-generation/gift-subscriptions/

**Contents:**
- Gift Subscriptions
  - Purchasing a Gift
  - Redeeming a Gift
    - Existing Paying Subscribers
  - Gift Reporting
    - Stripe
    - SendGrid

Gift subscriptions, which allow a person to buy a subscription for someone else, are now available on the Lede platform. By default, all of your products can be given as a gift.

There are a few different ways you can keep track of gift subscriptions, both purchases and redemptions.

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
If you have specialty products (in separate product groups) that you do not want available for gifting, please contact the Lede team by filing a support ticket.
```

Example 2 (unknown):
```unknown
The redemption codes associated with gifts expire one year after purchase.
```

---

## Social Sharing Call to Action (CTA)

**URL:** https://docs.joinlede.com/user-revenue-generation/social-sharing-call-to-action-cta/

**Contents:**
- Social Sharing Call to Action (CTA)

You can add text, encouraging users to share your content, next to the social sharing icons in the footer of single articles. This text applies to all articles on your site.

This text displays to the left of the social sharing icons in the footer of single article pages. This area can have a background color to further call attention to your message. This background color is the same as the color selected for highlighted posts on archive pages. To review/set this color:

Was this article helpful?

Thanks for the feedback!

---

## How to Use Promotional Pricing (including Coupon Codes)

**URL:** https://docs.joinlede.com/user-revenue-generation/how-to-use-promotional-pricing-including-coupon-codes/

**Contents:**
- How to Use Promotional Pricing (including Coupon Codes)
- To set up promotional pricing on your site
- Coupon Fields Template
- Things to be aware of
- Example Coupon Requests

You can offer your products on Lede at a discounted price point in order to drive initial subscription growth – these discounts can be offered to all new users who visit your Products page or only to new users who have a valid coupon code. Lede utilizes Stripe’s coupon functionality for this feature. To get this setup on your site, please review the information below.

Name (max 20 characters)

for billing, not coupon code

ID / coupon code (8-12 characters)

leave blank if promotion applies to all new users

Percentage or fixed amount

Monthly, annual, or all

The following are examples of requests that you might submit for various promotional pricing scenarios.

Scenario 1: Discounted fixed amount off price of one of your monthly products for three months – eligible only for users with a coupon code. After the discount expires, the subscription renews at the standard monthly price for the designated product.

Name: Dog Days of Summer Supporter Sale

Type: Fixed amount; $3.00 off

Products: Supporter (monthly option)

Redemption Limits: Date: August 31, 2023 at 11:59pm ET

Description: For a limited time, get $3 off your first 3 months of our Supporter plan.

Go Live Date & Time: July 3, 2023 at 12:01am ET

Name: Dog Days of Summer Supporter Sale

Type: Fixed amount; $3.00 off

Products: Supporter (monthly option)

Redemption Limits: Date: August 31, 2023 at 11:59pm ET

Description: For a limited time, get $3 off your first 3 months of our Supporter plan.

Go Live Date & Time: July 3, 2023 at 12:01am ET

Scenario 2: Discounted percent off price of all annual products for one year. After the discount expires, the subscription renews at the standard annual price for the designated product.

Name: Annual Holiday Sale

Type: Percentage; 10% off

Products: Lookout, Pal, and Benefactor (annual options)

Redemption Limits: December 31, 2024 at 11:59pm ET

Description: Happy holidays! Get 10% off of your first year on any of our annual products. Promo ends December 31, so act fast!

Go Live Date & Time: December 15, 2024 at 10am ET

Name: Annual Holiday Sale

Type: Percentage; 10% off

Products: Lookout, Pal, and Benefactor (annual options)

Redemption Limits: December 31, 2024 at 11:59pm ET

Description: Happy holidays! Get 10% off of your first year on any of our annual products. Promo ends December 31, so act fast!

Go Live Date & Time: December 15, 2024 at 10am ET

Scenario 3: Discounted fixed amount off price of the first month of one of your products. After the discount expires, the subscription renews at the standard annual level for the designated product.

Name: Mogul Madness Intro Sale

Type: Fixed amount; $25 off

Introductory Pricing: Yes – convert to annual subscription

Redemption Limits: March 31, 2023 at 11:59pm ET

Description: This month only, get $25 off of our Mogul annual subscription and all of its perks for one month. After the first month is up, renew at the standard annual plan price.

Go Live Date & Time: March 1, 2023 at 9am ET

Name: Mogul Madness Intro Sale

Type: Fixed amount; $25 off

Introductory Pricing: Yes – convert to annual subscription

Redemption Limits: March 31, 2023 at 11:59pm ET

Description: This month only, get $25 off of our Mogul annual subscription and all of its perks for one month. After the first month is up, renew at the standard annual plan price.

Go Live Date & Time: March 1, 2023 at 9am ET

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
You must notify us at least 24 hours in advance of needing your discounted products on your production site to ensure enough time for any clarifying questions we may have to ensure proper setup.
```

---

## Converting User Emails to Paying Subscribers

**URL:** https://docs.joinlede.com/user-revenue-generation/converting-user-emails-to-paying-subscribers/

**Contents:**
- Converting User Emails to Paying Subscribers
  - Email Campaign
  - Promotional Pricing Campaign
    - Coupon Codes
  - Ad Campaign (Sponsorship)
  - Adjust your Paywall Settings

There are a variety of ways you can approach converting users who have provided their email address to paying subscribers of your site.

If a user has provided their email address and has opted into receiving your newsletter, run an email campaign via SendGrid directed to these users.

To drive new user subscriptions, run a promotional pricing campaign which allows new users to purchase a subscription at a discounted rate.

Instead of running a promotional pricing campaign that is available to anyone who visits your site, consider a targeted campaign utilizing coupon codes for a specific group of users.

To drive users to your Products page, run an Ad Campaign which encourages users to subscribe.

Once a user has provided their email and is registered for your site, your paywall settings allow you to adjust how to encourage these users to become paying subscribers.

Was this article helpful?

Thanks for the feedback!

---
