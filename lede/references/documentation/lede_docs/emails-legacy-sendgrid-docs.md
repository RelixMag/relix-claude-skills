# Lede_Docs - Emails-Legacy-Sendgrid-Docs

**Pages:** 5

---

## Newsletter Builder in WordPress

**URL:** https://docs.joinlede.com/emails-legacy-sendgrid-docs/newsletter-builder-in-wordpress/

**Contents:**
- Newsletter Builder in WordPress
- Newsletter Builder: Initial Setup
- Newsletter Builder: Template Creation
- Newsletter Builder: Template Creation Tips
  - Newsletter Builder: Template Creation Tips – Post Blocks
    - Newsletter Single Post
    - Two Up Newsletter Post
    - Latest Posts
- Newsletter Builder: Newsletter Creation
- Newsletter Builder: Newsletter Creation Tips

The Newsletter Builder is a tool that allows you to construct reusable newsletter templates and create individual newsletters directly in WordPress, that are then sent out via SendGrid. You can easily include posts from your site in your newsletters – whether by curating specific posts, or sending out a list of recent posts or posts from a particular category.

To get started with the Newsletter Builder, populate the general settings which appear in the footer of all newsletters you send. This is a one-time setup, unless you need to make changes to these items.

In your WordPress Admin, navigation to Newsletters > General Settings > expand Footer Settings. Fill in the fields that you want to include in the Footer:

Social networks: Facebook, Twitter (X), Instagram, YouTube

Footer Image: Typically your logo

Company Address Line 1 and 2 (required to comply with anti-spam laws!)

Note: The words “Our mailing address is:” automatically display above your address in the footer.

Social networks: Facebook, Twitter (X), Instagram, YouTube

Footer Image: Typically your logo

Company Address Line 1 and 2 (required to comply with anti-spam laws!)

Note: The words “Our mailing address is:” automatically display above your address in the footer.

Note: The words “Our mailing address is:” automatically display above your address in the footer.

ℹ️ Note: A “Manage Subscription Preferences” link is automatically added to the bottom of the Newsletter Footer to ensure compliance with anti-spam laws. This link directs the user to their My Account page on your site so they can edit their newsletter preferences as desired. At this time, there is no direct “Unsubscribe” link – this will be available in a future update of the newsletter builder.

Next, construct the newsletter template(s) that you plan to reuse in the future for sending regular newsletters to your users. You can create as many templates as needed, based on the types of newsletters you typically send. Each template is a one-time setup, unless you need to make changes to the template.

In your WordPress Admin, navigate to Templates > Add New Post

Add title: Add an easily recognizable name for the template – this is for internal use only and does not display to end users.

Optional: Select Template Styles (in Template sidebar)

Background Color (default is white: #FEFEFE)

Link Color (default is blue: #0073AA)

Font Family (default is Arial)

The available fonts are all web/email-safe fonts that will display as expected in your sent emails in various email clients.

Build out newsletter template via the Block Inserter.

<whatever additional structural blocks are needed>

See below “Template Creation Tips” section for additional information on constructing your template.

Add title: Add an easily recognizable name for the template – this is for internal use only and does not display to end users.

Optional: Select Template Styles (in Template sidebar)

Background Color (default is white: #FEFEFE)

Link Color (default is blue: #0073AA)

Font Family (default is Arial)

The available fonts are all web/email-safe fonts that will display as expected in your sent emails in various email clients.

Background Color (default is white: #FEFEFE)

Link Color (default is blue: #0073AA)

Font Family (default is Arial)

The available fonts are all web/email-safe fonts that will display as expected in your sent emails in various email clients.

The available fonts are all web/email-safe fonts that will display as expected in your sent emails in various email clients.

Build out newsletter template via the Block Inserter.

<whatever additional structural blocks are needed>

See below “Template Creation Tips” section for additional information on constructing your template.

<whatever additional structural blocks are needed>

See below “Template Creation Tips” section for additional information on constructing your template.

See below “Template Creation Tips” section for additional information on constructing your template.

In your WordPress Admin, navigate to Newsletters > Email Types > Add Another Email Type

Fill in Label field (easily recognizable name of Email Type that typically corresponds 1:1 with your templates)

Image: Upload an image that will be used as the Header image in the newsletter

Under “Templates” check off the corresponding Template

Select “From Name” from dropdown

Note: These emails are pulled in directly from your SendGrid account – they are the authorized “single senders” in your account.

Fill in Label field (easily recognizable name of Email Type that typically corresponds 1:1 with your templates)

Image: Upload an image that will be used as the Header image in the newsletter

Under “Templates” check off the corresponding Template

Select “From Name” from dropdown

Note: These emails are pulled in directly from your SendGrid account – they are the authorized “single senders” in your account.

Note: These emails are pulled in directly from your SendGrid account – they are the authorized “single senders” in your account.

ℹ️ Note: There is often a 1:1 relationship between Email Type and Template, but you can have multiple Templates assigned to the same Email Type if desired. This allows you to reuse the same Header across templates.

Review the following tips for ease of future newsletter creation – while the specific content of your newsletters may drastically change with each newsletter you send, having a consistent template structure can drastically reduce the amount of design rework that is required going forward.

Include “Divider” and “Spacer” blocks directly in your template so you don’t need to manually add these blocks into every individual newsletter you send.

Once you have settled on a height and color for your “Divider” block and a height for your “Spacer” block, you can duplicate them and easily add them into various spots in your template – allowing you to create a consistent layout throughout your template.

How To: In the Block Inserter “List View”, click the kebab menu (3 vertical dots) to the right of your Divider/Spacer block and click “Duplicate”. Move the block to the desired location in the list.

Once you have settled on a height and color for your “Divider” block and a height for your “Spacer” block, you can duplicate them and easily add them into various spots in your template – allowing you to create a consistent layout throughout your template.

How To: In the Block Inserter “List View”, click the kebab menu (3 vertical dots) to the right of your Divider/Spacer block and click “Duplicate”. Move the block to the desired location in the list.

How To: In the Block Inserter “List View”, click the kebab menu (3 vertical dots) to the right of your Divider/Spacer block and click “Duplicate”. Move the block to the desired location in the list.

Most blocks have no default spacing added to the top/bottom, so use “Spacer” blocks throughout your template to ensure things look as you expect.

Supplement your Newsletter footer with additional information.

Add a “Newsletter Paragraph” block above your “Newsletter Footer” that contains Copyright information, along with any information you want to include about why the user is receiving the newsletter. You may also choose to include a way to sign up for the newsletter if the person had it sent to them by someone else.

Add a “Newsletter Paragraph” block above your “Newsletter Footer” that contains Copyright information, along with any information you want to include about why the user is receiving the newsletter. You may also choose to include a way to sign up for the newsletter if the person had it sent to them by someone else.

The “Newsletter Heading”, “Newsletter List”, and “Newsletter Paragraph” blocks all can have their text color adjusted and the “Newsletter Button” block can have its text and background color adjusted. Text color adjustments apply to all of the content within the block and cannot be applied to specific words within the block.

How To: In the Blocker Inserter “List View”, click the parent block (“Newsletter Heading”, “Newsletter List”, “Newsletter Paragraph”, or “Newsletter Button”). In the Block settings sidebar, select your desired Color from the color picker or enter a specific Hex Code in directly.

How To: In the Blocker Inserter “List View”, click the parent block (“Newsletter Heading”, “Newsletter List”, “Newsletter Paragraph”, or “Newsletter Button”). In the Block settings sidebar, select your desired Color from the color picker or enter a specific Hex Code in directly.

There are additional formatting options available on the “Newsletter Heading”, “Newsletter List”, “Newsletter Paragraph”, and “Newsletter Button” blocks. To view/adjust these options, click the block in the editor to view what is available in the quick edit menu which pops up above the block or in the Block settings sidebar.

Please note: The following quick edit text formatting options do NOT work:

Highlight, Inline image, Justify, Keyboard Input, Language

Please note: The following quick edit text formatting options do NOT work:

Highlight, Inline image, Justify, Keyboard Input, Language

Highlight, Inline image, Justify, Keyboard Input, Language

There are three Newsletter specific blocks which allow you to easily insert post content from your site. Placing them into your Newsletter Template allows you to streamline the newsletter creation process going forward.

This block allows you to curate a single post in your newsletter.

It contains a large featured image, the post headline, the post byline, the post excerpt (if available, else it’s the first few sentences of the post), and a Read More button.

It contains a large featured image, the post headline, the post byline, the post excerpt (if available, else it’s the first few sentences of the post), and a Read More button.

It is not recommended to curate the post within the template itself.

This block allows you to curate two posts in your newsletter.

It contains two posts that display side by side on desktop and in a single column on mobile.

It has all the same elements as the Newsletter Single Post block.

It contains two posts that display side by side on desktop and in a single column on mobile.

It has all the same elements as the Newsletter Single Post block.

It is not recommended to curate the posts within the template itself.

This block allows you to include a list of posts in your newsletter.

By default, a list of the five most recent post headlines displays, but you can add images, excerpts, dates, filter posts by category and/or author, and change the number of posts in the list.

By default, a list of the five most recent post headlines displays, but you can add images, excerpts, dates, filter posts by category and/or author, and change the number of posts in the list.

It is recommended that you configure the block settings within the template itself to streamline the newsletter creation process in the future.

After inserting this block, open up the block sidebar to review and adjust the settings as desired. All settings are optional.

Post content: Toggle this on and then click the radio button next to “Excerpt” to include the post’s excerpt. You can also set the max number of words that you want to display.

If you haven’t entered anything in the Excerpt field on the post, the max number of words you’ve selected will be pulled from the beginning of the post content display instead and will end with “…” in the email.

Display post date: This includes the date the post was published underneath the post headline.

Featured image: Toggle this on.

Select Resolution = Medium if you choose to align the images to the left or right.

Select Resolution = Large if you choose to align the images to the center.

Image alignment: Select Left, Center, or Right.

Toggle on “Add link to featured image”

This is highly recommended if you are including images in the post list, as this will allow users to click on the image to be brought directly to the post.

Sorting and filtering:

Order by: Select an option from the dropdown to change how the posts in the list are ordered. The default is Newest to Oldest.

Categories: Enter in the name of a category, or categories, that you want the post list to be filtered on. Only posts within those categories will display in the list.

Author: Select an author from the dropdown that you want the post list to be filtered on. Only posts from that author will display in the list.

Note: This list currently ONLY contains actual WordPress User accounts, not users who may have a byline on your site. All bylines will be available in a future update of the newsletter builder.

Number of items: Adjust the number of posts that you want to appear in the list – the slider goes from 1-100, but keep in mind that the majority of email clients will cut content off at some point. We recommend between 1-10 posts for most newsletters.

Post content: Toggle this on and then click the radio button next to “Excerpt” to include the post’s excerpt. You can also set the max number of words that you want to display.

If you haven’t entered anything in the Excerpt field on the post, the max number of words you’ve selected will be pulled from the beginning of the post content display instead and will end with “…” in the email.

If you haven’t entered anything in the Excerpt field on the post, the max number of words you’ve selected will be pulled from the beginning of the post content display instead and will end with “…” in the email.

Display post date: This includes the date the post was published underneath the post headline.

Display post date: This includes the date the post was published underneath the post headline.

Featured image: Toggle this on.

Select Resolution = Medium if you choose to align the images to the left or right.

Select Resolution = Large if you choose to align the images to the center.

Image alignment: Select Left, Center, or Right.

Toggle on “Add link to featured image”

This is highly recommended if you are including images in the post list, as this will allow users to click on the image to be brought directly to the post.

Select Resolution = Medium if you choose to align the images to the left or right.

Select Resolution = Large if you choose to align the images to the center.

Select Resolution = Medium if you choose to align the images to the left or right.

Select Resolution = Large if you choose to align the images to the center.

Image alignment: Select Left, Center, or Right.

Toggle on “Add link to featured image”

This is highly recommended if you are including images in the post list, as this will allow users to click on the image to be brought directly to the post.

This is highly recommended if you are including images in the post list, as this will allow users to click on the image to be brought directly to the post.

Sorting and filtering:

Order by: Select an option from the dropdown to change how the posts in the list are ordered. The default is Newest to Oldest.

Categories: Enter in the name of a category, or categories, that you want the post list to be filtered on. Only posts within those categories will display in the list.

Author: Select an author from the dropdown that you want the post list to be filtered on. Only posts from that author will display in the list.

Note: This list currently ONLY contains actual WordPress User accounts, not users who may have a byline on your site. All bylines will be available in a future update of the newsletter builder.

Number of items: Adjust the number of posts that you want to appear in the list – the slider goes from 1-100, but keep in mind that the majority of email clients will cut content off at some point. We recommend between 1-10 posts for most newsletters.

Order by: Select an option from the dropdown to change how the posts in the list are ordered. The default is Newest to Oldest.

Categories: Enter in the name of a category, or categories, that you want the post list to be filtered on. Only posts within those categories will display in the list.

Author: Select an author from the dropdown that you want the post list to be filtered on. Only posts from that author will display in the list.

Note: This list currently ONLY contains actual WordPress User accounts, not users who may have a byline on your site. All bylines will be available in a future update of the newsletter builder.

Note: This list currently ONLY contains actual WordPress User accounts, not users who may have a byline on your site. All bylines will be available in a future update of the newsletter builder.

Number of items: Adjust the number of posts that you want to appear in the list – the slider goes from 1-100, but keep in mind that the majority of email clients will cut content off at some point. We recommend between 1-10 posts for most newsletters.

IMPORTANT: The following settings in this block should NOT be used:

Post Content: Show Full post

Post Meta: Display author name

Width/height manual inputs

Width/height percentage selections

Resolution = Thumbnail

Image Alignment: None

Post Content: Show Full post

Post Meta: Display author name

Width/height manual inputs

Width/height percentage selections

Resolution = Thumbnail

Image Alignment: None

Width/height manual inputs

Width/height percentage selections

Resolution = Thumbnail

Image Alignment: None

Once your one-time setup items are complete, you can now create your individual newsletters to send to your users.

In your WordPress Admin, navigation to Newsletters > Add New Post

Add title: Add a Title to the Newsletter (this displays in SendGrid also) – this is for internal use only and does not display to end users.

Select Header Type: This is the Email Type of the newsletter you plan to send. Once selected, the “Select Template” and “From Name” fields should populate based on your selection.

Subject: Enter in a Subject for your newsletter

Preview Text: Enter in preview text for your newsletter (this is the short summary text that typically displays below/after the subject line in email inboxes)

Email list: Select the email list(s) you want to send this newsletter to.

Note: These email lists are pulled in directly from your SendGrid account – they are the “Lists” which display on your Contacts List page.

At this time only Lists are available; segments will be available in a future update of the newsletter builder.

You can select multiple lists, if needed.

Suppression Group: Select the suppression group (also called an “unsubscribe group” in portions of the SendGrid dashboard) containing contacts who have unsubscribed from this list. The typical convention is to name the unsubscribe group the same thing as the list itself.

Edit Newsletter Contents as desired

See below “Newsletter Creation Tips” section for additional information on creating your newsletter

Clicking “Publish” sends the newsletter out right away.

Once published, your newsletter will appear in the “Newsletters” list in the WordPress Admin and will also appear in SendGrid.

Optionally, you can schedule your newsletter to be sent out at a particular time, just as you would schedule a post.

How To: Click the word “Immediately” next to Publish in the Newsletter sidebar and select the date/time from the date picker. Click “Schedule…” which takes the place of the Publish button.

Once scheduled, your newsletter will appear in the “Newsletters” list in the WordPress Admin as a Scheduled post, and won’t appear in SendGrid until the scheduled time arrives.

Add title: Add a Title to the Newsletter (this displays in SendGrid also) – this is for internal use only and does not display to end users.

Select Header Type: This is the Email Type of the newsletter you plan to send. Once selected, the “Select Template” and “From Name” fields should populate based on your selection.

Subject: Enter in a Subject for your newsletter

Preview Text: Enter in preview text for your newsletter (this is the short summary text that typically displays below/after the subject line in email inboxes)

Email list: Select the email list(s) you want to send this newsletter to.

Note: These email lists are pulled in directly from your SendGrid account – they are the “Lists” which display on your Contacts List page.

At this time only Lists are available; segments will be available in a future update of the newsletter builder.

You can select multiple lists, if needed.

Note: These email lists are pulled in directly from your SendGrid account – they are the “Lists” which display on your Contacts List page.

At this time only Lists are available; segments will be available in a future update of the newsletter builder.

You can select multiple lists, if needed.

Suppression Group: Select the suppression group (also called an “unsubscribe group” in portions of the SendGrid dashboard) containing contacts who have unsubscribed from this list. The typical convention is to name the unsubscribe group the same thing as the list itself.

Edit Newsletter Contents as desired

See below “Newsletter Creation Tips” section for additional information on creating your newsletter

See below “Newsletter Creation Tips” section for additional information on creating your newsletter

Clicking “Publish” sends the newsletter out right away.

Once published, your newsletter will appear in the “Newsletters” list in the WordPress Admin and will also appear in SendGrid.

Clicking “Publish” sends the newsletter out right away.

Once published, your newsletter will appear in the “Newsletters” list in the WordPress Admin and will also appear in SendGrid.

Optionally, you can schedule your newsletter to be sent out at a particular time, just as you would schedule a post.

How To: Click the word “Immediately” next to Publish in the Newsletter sidebar and select the date/time from the date picker. Click “Schedule…” which takes the place of the Publish button.

Once scheduled, your newsletter will appear in the “Newsletters” list in the WordPress Admin as a Scheduled post, and won’t appear in SendGrid until the scheduled time arrives.

Optionally, you can schedule your newsletter to be sent out at a particular time, just as you would schedule a post.

How To: Click the word “Immediately” next to Publish in the Newsletter sidebar and select the date/time from the date picker. Click “Schedule…” which takes the place of the Publish button.

Once scheduled, your newsletter will appear in the “Newsletters” list in the WordPress Admin as a Scheduled post, and won’t appear in SendGrid until the scheduled time arrives.

ℹ️ Note: Once published, it takes about 1-2 minutes for the newsletter to go from WordPress to SendGrid to your inbox.

Review the following tips for creating your individual newsletter:

The “Newsletter Heading”, “Newsletter List”, and “Newsletter Paragraph” blocks all can have their text color adjusted and the “Newsletter Button” block can have its text and background color adjusted. Text color adjustments apply to all of the content within the block and cannot be applied to specific words within the block.

How To: In the Blocker Inserter “List View”, click the parent block (“Newsletter Heading”, “Newsletter List”, “Newsletter Paragraph”, or “Newsletter Button”). In the Block settings sidebar, select your desired Color from the color picker or enter a specific Hex Code in directly.

How To: In the Blocker Inserter “List View”, click the parent block (“Newsletter Heading”, “Newsletter List”, “Newsletter Paragraph”, or “Newsletter Button”). In the Block settings sidebar, select your desired Color from the color picker or enter a specific Hex Code in directly.

There are additional formatting options available on the “Newsletter Heading”, “Newsletter List”, “Newsletter Paragraph”, and “Newsletter Button” blocks. To view/adjust these options, click the block in the editor to view what is available in the quick edit menu which pops up above the block or in the Block settings sidebar.

Please note: The following quick edit text formatting options do NOT work:

Highlight, Inline image, Justify, Keyboard Input, Language

Please note: The following quick edit text formatting options do NOT work:

Highlight, Inline image, Justify, Keyboard Input, Language

Highlight, Inline image, Justify, Keyboard Input, Language

It is not currently possible to place an image NEXT to text. This will be available in a future update of the newsletter builder.

Newsletter Single Post and Two Up Newsletter Post

You can curate specific posts for these blocks by clicking the “Select” button and then search for the post via the Post Picker modal which pops up. To change your curated post, click the red “X” in the top right corner of the post.

Once you have selected a post, you can override all aspects of the post: image, title, byline, and except. You can also edit the text of the “Read More” button which displays.

You can curate specific posts for these blocks by clicking the “Select” button and then search for the post via the Post Picker modal which pops up. To change your curated post, click the red “X” in the top right corner of the post.

Once you have selected a post, you can override all aspects of the post: image, title, byline, and except. You can also edit the text of the “Read More” button which displays.

You have likely configured this block within the template itself, but you can make changes to any of the configuration settings in the block sidebar within the newsletter if needed. Please refer to the above section about the Latest Post block for a full overview of block settings, including what settings to avoid using.

You have likely configured this block within the template itself, but you can make changes to any of the configuration settings in the block sidebar within the newsletter if needed. Please refer to the above section about the Latest Post block for a full overview of block settings, including what settings to avoid using.

The Newsletter Builder also provides the ability to quickly send out a single article to your users – consider using this for breaking news, big site updates, or other content you want your users to quickly get directly in their inbox. You can do this when a post is being published/scheduled, or after a post has already been published.

Create a new Email Type & corresponding Template specifically for Single Article Sends (or perhaps more than one, depending on what type of content you plan to send in this manner).

In your template, the following blocks must be included:

Newsletter Single Post

Include any desired styling as well. For full email type/template creation instructions, refer to the above “Template Creation” steps.

Once you’ve created your Single Send Email Type & Template, do the following to send an individual article to your users.

In the post editor of the post you wish to send to your users, click the envelope (Newsletter) icon in the top right corner (directly to the right of the blue Publish/Update button).

In the Newsletter sidebar

Select the “Header Type” (this is the Email type you want to use for the individual post)

Select the “Template”

Ensure the proper “From Name” is selected

Edit the “Subject” field as desired (the title of the post appears by default, but can be changed, if needed)

Edit the “Preview Text” field as desired (this is the short summary text that typically displays below/after the subject line in email inboxes)

Select the Email List(s) you want to send this newsletter to.

Check off “Send Newsletter on Publish/Update”

Note: This option is grayed out if any required newsletter settings are missing – check for any red messages underneath “Newsletter Validation” if this is the case.

Select the “Header Type” (this is the Email type you want to use for the individual post)

Select the “Template”

Ensure the proper “From Name” is selected

Edit the “Subject” field as desired (the title of the post appears by default, but can be changed, if needed)

Edit the “Preview Text” field as desired (this is the short summary text that typically displays below/after the subject line in email inboxes)

Select the Email List(s) you want to send this newsletter to.

Check off “Send Newsletter on Publish/Update”

Note: This option is grayed out if any required newsletter settings are missing – check for any red messages underneath “Newsletter Validation” if this is the case.

Note: This option is grayed out if any required newsletter settings are missing – check for any red messages underneath “Newsletter Validation” if this is the case.

Optional, but recommended: In the Post sidebar, enter in an Excerpt which will display in the email itself.

Note: If you don’t enter anything here, the first few sentences of the post content will display instead and will be cut off with a […] in the email.

Note: If you don’t enter anything here, the first few sentences of the post content will display instead and will be cut off with a […] in the email.

Optional, but recommended: In the Post sidebar, ensure your post has a Featured Image which will display in the email itself.

Note: If you don’t add a featured image, no image will be displayed in the email for the post.

Note: If you don’t add a featured image, no image will be displayed in the email for the post.

Click Publish/Update when ready.

Once published, your newsletter will appear in the “Newsletters” list in the WordPress Admin and will also appear in SendGrid – the title of the newsletter will be prefaced by “Breaking News” in these locations.

Note: The single sends functionality also works when scheduling a post to be published.

Once published, your newsletter will appear in the “Newsletters” list in the WordPress Admin and will also appear in SendGrid – the title of the newsletter will be prefaced by “Breaking News” in these locations.

Note: The single sends functionality also works when scheduling a post to be published.

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (typescript):
```typescript
It is highly recommended that you send a test newsletter to yourself before sending to your users, to ensure your newsletter is formatted as you expect. To do this, you can add yourself to a separate test List in SendGrid and send the newsletter to that newly created List.
```

Example 2 (sql):
```sql
Email Newsletter formatting can be very unforgiving. If you copy/paste text from another source (such as a Word document) into WordPress, formatting can sometimes be copied over along with the content. It is advised that you remove this formatting, as not all formatting which is allowable in a Word document or on your site, will display as expected in an email.
```

---

## SendGrid Overview

**URL:** https://docs.joinlede.com/emails-legacy-sendgrid-docs/sendgrid-overview/

**Contents:**
- SendGrid Overview
- Adding team members
- Marketing
  - Automations
  - Single Sends
  - Contacts
  - Signup Forms
- Stats
- Activity
- Other settings

Lede uses SendGrid to create and send newsletters, manage newsletter subscriber lists, set up email automations, and send automated emails from the platform.

You can log in to SendGrid here.

You can add users to your account to let staff members manage email.

Go to Settings → Teammates → Add teammate → Add password teammate, then follow the prompts to invite a user at the appropriate permission level.

Automated emails and email sequences can be configured to run when a user is added to a list or a segment.

Single Sends are mainly used for sending out newsletters to your registered users and/or subscribers.

Contacts contains all your Lists, Segments, and the individual users who comprise those Lists & Segments. In addition, Unsubscribe Groups need to be maintained in order to honor your recipients’ email preferences and protect your sender reputation by complying with anti-spam legislation.

Create a standalone sign-up form for a newsletter list that will allow subscribers to directly sign up for a newsletter, bypassing the site newsletter/login flow.

At this time, users who sign up directly via SendGrid will not be represented in your Stripe account or the Lede CDP.

SendGrid provides a number of stats pertaining to your email performance, including:

There are also a number of stats pertaining to subscriber data, including:

This is a great place for troubleshooting if subscribers are reporting any issues with email delivery.

Entering the user’s email and the date range the issue is being reported for will allow you to see any email activity for that user and potentially track down their issue. Note that even if an email is marked “Delivered” in SendGrid, the email may end up in spam, an alternate inbox, or an issue outside of SendGrid could be preventing the email from being delivered.

An email may take some time to appear in the activity log if it was just sent, especially in the case of account-based emails for account logins and verification.

Your SendGrid account is attached to the parent Lede SendGrid account. You’ll only see settings related to your own account, and you won’t be able to access billing-related information.

Was this article helpful?

Thanks for the feedback!

---

## Annual Subscription Renewal Emails

**URL:** https://docs.joinlede.com/emails-legacy-sendgrid-docs/annual-subscription-renewal-emails/

**Contents:**
- Annual Subscription Renewal Emails
  - Custom Template
    - Variables & Conditionals
  - Default Template

In addition to being able to customize the renewal email to better represent your site’s offerings, you can further personalize the emails for your users, including their renewal date and what product they are subscribed to. These variables (besides URL) can also be added to the subject of the email.

Furthermore, you can add conditional text for all users subscribed to a particular product. For example,

You can also add conditional images for all users subscribed to a particular product. To do this:

If you do not create a custom email for this, a default template is sent to your subscribers. The text of that email can be seen below.

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
In the examples above, replace "ABC Product" or "Product Group YYZ" with the exact name of your product or product group. If you are unsure, please contact the Lede team.
```

---

## Prerequisites for Sending Email with SendGrid

**URL:** https://docs.joinlede.com/emails-legacy-sendgrid-docs/prerequisites-for-sending-email-with-sendgrid/

**Contents:**
- Prerequisites for Sending Email with SendGrid

After you have read the general overview of SendGrid, be sure to review how to send email with SendGrid for a detailed look into how to configure your first newsletter or email campaign. As you will see there are a few important prerequisites to set up to ensure your first email campaign runs smoothly, such as:

You should also take some time to determine your newsletter strategy. Consider the following:

In SendGrid you may create either single send email campaigns (one-time only) or recurring emails with automations. See the following pages for an overview of both:

Was this article helpful?

Thanks for the feedback!

---

## SendGrid: Single Sends Overview

**URL:** https://docs.joinlede.com/emails-legacy-sendgrid-docs/sendgrid-single-sends-overview/

**Contents:**
- SendGrid: Single Sends Overview
- 1. Select a Design
- 2. Select an Editor
- 3. Configure Single Send Settings
  - Single Send Settings
  - Recipients
  - Schedule
  - Test Your Email
- 4. Build Your Newsletter
- 5. Review Details and Send Your Newsletter

In SendGrid, Single Sends are typically used for sending out your newsletters to your registered users and/or subscribers. To compose and send your newsletters in SendGrid, click Marketing > Single Sends.

First, create or select the design for your newsletter. For detailed documentation on designing and setting up a template, check out SendGrid’s documentation on email designs. You may choose an existing template you have already created or customize one from SendGrid’s Design Library.

Next, select which Editor you will use for editing your newsletter: the Design Editor or the Code Editor. The Design Editor is recommended unless you have familiarity and comfort with editing HTML directly.

Single Send Name: This is an internal only name that will not be displayed within the email itself. Use this to clearly label your Single Sends.

From Sender: Select from the list of Senders you have added. This information is publicly visible and informs users who the email is coming from.

Subject: This is the publicly visible email subject which encourages users to open your newsletter.

Preheader: This is the publicly visible short summary text which typically displays after the Subject in email inboxes.

Categories: This is an internal only, optional designation that is used for organizational purposes.

The Recipients Settings determine the list of subscribers you’ll be sending to and the unsubscribe behavior in the footer of that email.

Send To: Each newsletter you have configured on Lede will appears in this dropdown. Select the relevant list for your newsletter.

Exclude specific recipients: If you want to further target subscribers or non-subscribers, you can exclude recipients based on segments. For instance, you can send one version of your free newsletter to the Newsletter list and exclude a segment of paying subscribers — that newsletter could include calls to action to purchase a subscription. You can then send another version of your free newsletter to the same Newsletter list and exclude a segment of non-paying users, which would leave out those calls to action.

Unsubscribe Group: Select the unsubscribe group related to the newsletter you’re sending. In the case of marketing emails, you should use a specific unsubscribe group for “Updates” or something similar. The unsubscribe group determines what the user ends up unsubscribed from when they click the link at the bottom of the email. Using the global unsubscribe group will result in the user being removed from all emails except for transactional emails, so consistent usage of unsubscribe groups will help avoid that.

You can choose to send your email immediately or you can schedule it for a specific date and time.

Before sending your email, you can test it to ensure it looks as you expect. You can enter your email to “Send a Test Email” after you have added content to your email.

Depending on the type of Editor you have selected, you will be able to build your newsletter with modules & global styles (Design Editor) or completely customize the HTML (Code Editor).

When you have finished configuring your newsletter settings and adding your newsletter content, consider testing your email by sending yourself a test email. Then click Review Details and Send. Ensure all of your settings are correct and your newsletter looks as you expect. Click Send or Schedule, depending on which option you have selected, when you are ready!

Was this article helpful?

Thanks for the feedback!

---
