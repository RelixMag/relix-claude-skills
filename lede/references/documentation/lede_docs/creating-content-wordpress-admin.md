# Lede_Docs - Creating-Content-Wordpress-Admin

**Pages:** 27

---

## Ticker Block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/ticker-block/

**Contents:**
- Ticker Block
- Ticker Block
- Availability
- Setup
- How It Works
- Color Behavior
- Accessibility
- Use Cases

The Ticker block displays a continuously scrolling line of text across the full width of the page, similar to a news ticker or stock market marquee. It’s a great way to draw attention to timely announcements, promotions, or editorial highlights.

The Ticker block is available on pages and reusable blocks. It is not available on posts.

To add a Ticker block, open the block inserter in the page editor and look for “Ticker” under the Lede category. Once added, enter your text in the text field. Bold and italic formatting are supported.

To customize the block’s appearance, use the color settings in the block sidebar. Background and text colors can be set independently.

To display the block flush against the site header or footer, find Page Layout Options in the Page sidebar and toggle on “Extend layout to header” or “Extend layout to footer.”

Note: Your text may wrap to multiple lines in the editor, but it will scroll as a single line on the front end.

The block scrolls your text from right to left across the screen at a consistent speed, regardless of text length. A pause/play button is included so readers can stop the animation and read the text at their own pace.

In light mode, the block uses the colors you’ve selected in the editor. If no colors are set, it defaults to a light grey background with black text.

In dark mode, the block uses dark theme colors regardless of what was selected in the editor. This ensures consistent readability across both modes.

The Ticker block is designed with accessibility in mind. A pause/play button lets readers stop and restart the animation, and the button is fully keyboard accessible. If a reader has reduced motion enabled in their system preferences, the text will not scroll. Screen readers receive a static version of the text rather than the scrolling animation.

The Ticker block works well for breaking news or developing story alerts, event promotions or countdowns, subscription or membership calls to action, sponsor or partner messaging, and editorial commentary or highlighted quotes.

Was this article helpful?

Thanks for the feedback!

---

## Creating Content

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/

**Contents:**
- Creating Content
  - Affiliate Block
  - Author Bylines
  - Custom Embed Block
  - Default Featured Image
  - Embed Blocks Overview
  - Embeddable Forms forms for Contact Us pages, etc.
  - Essential WordPress Shortcuts for Content Creators
  - Featured Authors Block
  - Featured Post Block: Examples Gallery

Was this article helpful?

Thanks for the feedback!

---

## Author Bylines

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/author-bylines/

**Contents:**
- Author Bylines

For attributing author bylines to a post, see the post fields article. For byline display options, see the Byline Display Customization article.

In WordPress, a user is an individual who has an account on your website and has access to the WordPress dashboard, where they can manage their profile, posts, and other content. When a user creates a post they are considered by WordPress to be the post’s “author.”

However, the creator of a post is not necessarily the author of the post’s content, i.e. the article’s text, so the Lede platform has introduced bylines. The author byline will display their name and image (if available) and will link to their author bio page on the site.

Available bylines come from Profiles in the WordPress dashboard. A profile is a collection of information about an individual, such as their name, email address, bio, and website.

The main difference between users and profiles is that users have access to the WordPress dashboard, while profiles do not necessarily. (Although it’s common for users to have profiles, which they can edit themselves). Only users can create and edit posts, pages, and other content, while a post’s authorship can be attributed to any profile via bylines.

Creating & Updating Profiles

Was this article helpful?

Thanks for the feedback!

---

## Page Layout Options

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/page-layout-options/

**Contents:**
- Page Layout Options
- Finding the Page Layout Options
- Understanding the Three Layout Controls
  - 1. Extend Layout to Header
  - 2. Hide Title
  - 3. Extend Layout to Footer
- Important Considerations
  - Advertising and Sponsorships
  - Homepage Behavior
- Design Tips for Maximum Impact

The Page Layout Options panel gives you powerful tools to create visually striking pages by controlling spacing and title display. This feature, exclusive to pages (not available on posts), lets you craft seamless layouts perfect for homepages and featured pages (such as annual reports).

Navigate to your page editor and locate the Page sidebar. Within the sidebar, you’ll find the Page Layout Options panel containing three simple toggle switches that control your page’s visual presentation.

This option removes the default spacing between your site header and the first content block on the page. When enabled, your content flows seamlessly from the navigation area, creating a cohesive, professional appearance.

Toggle this switch to prevent the page title from appearing on the front end of your site. This gives you complete control over your page hierarchy and visual flow, allowing hero images or custom headers to take center stage.

Similar to the header option, this setting eliminates the gap between your last content block and the site footer, creating a smooth transition to your footer content.

Before implementing these layout options, keep these key points in mind:

Leaderboard ads and banner sponsorships take precedence over the “Extend layout to header” setting. If you have advertising enabled at the top of your page, the system will maintain appropriate spacing between the ad unit and your first content block, regardless of your layout settings.

The homepage and pages using the homepage layout template automatically hide titles by default. You don’t need to enable the “Hide title” option for these pages—it’s already taken care of for you.

Full-width content blocks create the most dramatic effect when combined with extended header and footer layouts. These blocks stretch edge-to-edge across the screen, eliminating visual boundaries and creating an immersive experience.

The editor view doesn’t fully represent how your extended layouts will appear on the live site. Always use the preview function to see exactly how your design choices will look to visitors. This ensures you’re confident in your layout decisions before making them public.

Ready to transform your pages? Open any page in your editor, locate the Page Layout Options panel in the sidebar, and experiment with different combinations. Remember to preview your changes and consider how each option enhances your content’s presentation.

With these simple yet powerful controls, you’re equipped to create pages that not only inform but also inspire your visitors through thoughtful, professional design.

Was this article helpful?

Thanks for the feedback!

---

## Post Blocks Overview

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/post-blocks-overview/

**Contents:**
- Post Blocks Overview

Blocks are the components for adding content to your posts.

Manually adding an Ad Unit block to a post will display a 300 x 250 article ad from Google Ad Manager between blocks of content. Google Ad Manager must be configured in order to use this block. Setting this up can be self-served or configured with Lede’s assistance.

This block prompts your readers to sign up for your newsletter. Lede uses SendGrid to create and send newsletters.

Additionally, please see methods for converting user emails into paying subscribers.

Finally, the Newsletter block can be regularly reused with specific styling or configurations so our guide on reusable blocks is also quite useful.

This block allows you to display a related post. You can curate a related post by selecting a post via the Post Picker in the settings sidebar. If uncurated, the most recent post in the same primary category as this article will display.

Was this article helpful?

Thanks for the feedback!

---

## Default Featured Image

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/default-featured-image/

**Contents:**
- Default Featured Image
- Why Use a Default Featured Image?
- How to Set a Default Featured Image
- Best Practices for Choosing Your Default Image

A default Featured Image can be set in the Customizer. This image is used in post cards when there is no Featured Image set in a post.

Setting a default Featured Image helps maintain visual consistency across all post cards and pages, giving your site a polished, professional appearance. Post cards with images are more visually engaging and easier to scan than text-only cards, creating a better experience for your readers.

To set a default featured image, go to Appearance > Customize > Site Identity. Then scroll down to Default Featured Image. Unless you are using square images across your site, we recommend an aspect ratio of 3:2.

Keep it generic and versatile – Choose an image that won’t clash with any particular post topic. Abstract patterns, subtle textures, or minimalist designs work well.

Incorporate branding elements – Include your logo, brand colors, or visual style so the default image reinforces your identity.

Ensure readability – If text overlays the image, choose one with appropriate contrast and clear areas where headlines remain legible. Avoid busy images that compete with text.

Match your site’s aesthetic – The default image should feel cohesive with your overall design and reflect your content niche.

Was this article helpful?

Thanks for the feedback!

---

## How to Use Reusable Blocks (Synced Patterns)

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/how-to-use-reusable-blocks-synced-patterns/

**Contents:**
- How to Use Reusable Blocks (Synced Patterns)
- How to use Reusable Blocks:
- How to View and Manage All of Your Reusable Blocks
- Alternative approach to using Reusable Blocks

Reusable blocks, now called Synced Patterns, are useful when you want to regularly reuse a particular block with specific styling and other settings or when you want to reuse a specific configuration of blocks.

One of the primary use cases for this feature is for customized newsletter blocks that are placed in posts on a recurring basis.

Was this article helpful?

Thanks for the feedback!

---

## Spotlight: Featured Post block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/spotlight-featured-post-block/

**Contents:**
- Spotlight: Featured Post block
- ⚙️ Settings
  - Post Picker
  - Image Options
  - Byline Options
  - Category Eyebrow
  - Lede Lite
- ◐ Styles
  - Color
  - Typography

The Featured Post block highlights a single story in an eye-catching way, making it perfect for drawing attention to your most important content. When added to your homepage or any page, this block displays a post’s featured image, title, subtitle/dek (if used), and byline in a visually compelling format.

The block offers flexible configuration options through both the block sidebar and toolbar, allowing you to customize its appearance to match your site’s design and content strategy.

See the Featured Post Block in Action →

Select which post to feature using the post picker module. If no post is selected, the block will automatically display a backfilled post to ensure your page never appears empty.

Control how author information appears:

Display a linked category label above the image to help readers navigate related content.

Enable a text-only version featuring an oversized headline—ideal for creating visual hierarchy without imagery.

Customize the text and background colors to create contrast or match your brand palette.

Customize the Featured Post block’s heading

Fine-tune the block’s spacing:

Quick-access options include:

Was this article helpful?

Thanks for the feedback!

---

## Post/Page Fields Overview

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/post-page-fields-overview/

**Contents:**
- Post/Page Fields Overview
- Post/Page option beneath the main Post Editor

Page/Post Fields in the Block Settings sidebar

The Page/Post settings sidebar contains several fields used to customize the main aspects of the page or post that is being published. It is part of the WordPress Block Editor on pages and posts.

To open, select the Settings icon on the upper right navigation bar. Within the menu, the left tab will display the fields and other options for the entire Page or Post you are editing, while the right tab will display the settings for the individual Block selected. Not all available options in the Editor are compatible with the Lede platform – see below for information on each option.

Visibility controls how this post is viewed once it is published.

Publish This setting controls when a post will be published. Select Now and the post will be published immediately. You can also schedule a post to be published in the future, or backdate the publication of a post, by selecting a time and date.

Template Detailed information on how to create, set and manage templates.

URL This setting allows you to edit the Permalink, or permanent URL, for the page or post. Clicking on the current setting for the URL will open a menu where you can change the settings:

Stick to top of blog This option is not compatible with the Lede platform.

Pending review The pending review checkmark indicates that the page/post is ready for someone to review it. Posts that are pending review are marked as Pending in the list of posts and will also show up in the filter under Pending. This checkbox will not be available once a page/post is published.

Author This field displays the creator of a post or page. (Not to be confused with byline, the writer of an article credited on the public facing post.) You can change the author by selecting a different author from the dropdown list. Author names are populated by Users in the WordPress Admin of your site. Navigate to Users to create new authors.

Byline The byline names the writer of the article and appears on the public post. Bylines can be found or created under Profiles in the WordPress Admin of your site. Within the post’s settings sidebar, the following options are available.

Switch to Draft Click this button to unpublish the post.

Move to Trash Click this button to move the post to the Trash.

Newsletter Visibility This option is a Jetpack feature that is not compatible with the Lede platform.

Open Graph This option is not compatible with the Lede platform. Reference the “Yoast SEO” settings below instead.

Revisions Display the number of times the post was revised. Clicking this number will take you to a new view where you can compare any two revisions side by side.

Categories Categories provide a helpful way to group related posts together. They not only help keep posts organized, but you can also use categories to display posts in several places across your site, making it easier for your users to find what they’re looking for quickly.

Tags Tags provide another useful way to group related posts together and quickly tell your readers what a post is about. Unlike Categories, Tags are not required for posts. Any selected Tags display in alphabetical order at the end of a post next to a “Read More” label.

Featured Image To set the Featured Image, drag an image from your computer and drop it in the gray box. You can also click the Set featured image box, which opens the Media Library where you can select the image or upload a new image. Other options include:

Posts ONLY: Featured image variants

Excerpt Here you can write a one to two sentence description of the post or page. This information is used as the fallback excerpt field in your RSS feeds and can be displayed in the Post River block.

Dek Here you can enter a brief subhead of a post as a way to entice your users to read the entire article. If the Dek field is filled out, it displays below the headline on the post itself, in the Post River, and in the Featured Post block on the Homepage. The Dek field supersedes the Excerpt field in RSS feeds as mentioned above.

Was this article helpful?

Thanks for the feedback!

---

## Featured Post Block: Examples Gallery

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/featured-post-block-examples-gallery/

**Contents:**
- Featured Post Block: Examples Gallery
- Example 1: With background color, full width, no byline
- Example 2: With default byline, 3:2 image, subtitle/dek
- Example 3: With category eyebrow
- Example 4: With outline, no subtitle
- Example 6: With centered text
- Example 7: With secondary font used in heading

See the Featured Post block in action! This gallery showcases real-world examples of how you can use this versatile block to highlight your most important content. Explore different configurations, color schemes, layouts, and styling options to find inspiration for your own site.

For detailed instructions on configuring each option, visit our Featured Post Block Knowledge Base article.

Courtesy of Gazetteer San Francisco

Example 5: Square image, inside a column

Courtesy of Stereogum

Courtesy of Sox Machine

Was this article helpful?

Thanks for the feedback!

---

## The Engagement Block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/the-engagement-block/

**Contents:**
- The Engagement Block
- Quick Start
  - What it does
  - Set it up in 4 steps
  - The one setting to know
  - Good to know
- Full Details
  - How it works
  - When to use it
  - How to use it

The Engagement Block is a smart, audience-aware container you can drop into your homepage, single pages, and single articles. Instead of showing the same call-to-action to everyone, it automatically shows a different view depending on who’s reading — so you never ask an existing subscriber to “subscribe” again, and you can thank paying readers instead of pitching them.

One block, three audiences, the right ask for each.

One block automatically shows a different call-to-action depending on who’s reading:

On the live site, each reader sees only the one view that matches them.

In the sidebar, the Audience routing panel lets you choose what each audience sees:

Any view can go to any audience, and Hide shows nothing to that group. Leave the defaults if you just want Newsletter → Subscribe → Tip.

The block comes with three built-in views — Newsletter, Subscribe, and Tip — and you decide which view each audience sees, or whether they see nothing at all.

Each view contains a heading, a paragraph, an optional image, and a call-to-action — a sign-up form in the Newsletter view, and a button in the Subscribe and Tip views.

Important: In the editor, you use the preview toggle to switch between and design each view one at a time. On the live site, only one view ever renders per reader — the one routed to their audience.

Audience routing panel — decide what each audience sees:

Every view is selectable for every audience, plus a Hide option to render nothing for that group.

Editor preview panel:

Styling (applies to the container, shared by whichever view shows):

The CTA button is a flexible Button Link with full styling controls:

Was this article helpful?

Thanks for the feedback!

---

## Guide to the Media Card block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/guide-to-the-media-card-block/

**Contents:**
- Guide to the Media Card block
- About
- What’s Inside this Block
- Block Availability
- Initial Block Setup
- Pro Tips & Best Practices
- Examples
  - Mobile – Light Mode
  - Desktop – Light Mode
- Desktop – Dark Mode

A compact, versatile component that showcases content through three key elements: a visual image, a descriptive heading, and multiple action links. This component can be used to highlight books, albums, videos, products, team members, events, or any content that benefits from visual representation with multiple access points

Works well with the Flex List Item to create eye-catching listicles.

The block includes an image, a heading, and optional links or sources.

The image has a maximum width of 200px on desktop and a maximum width of 100% of mobile.

There are no settings for the this block.

This block is available on Posts and Pages.

The block contains placeholder content for the image, heading, and three sources. The source placeholders can be removed; additional sources can be added.

Was this article helpful?

Thanks for the feedback!

---

## Guide to the Flex List Item block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/guide-to-the-flex-list-item-block/

**Contents:**
- Guide to the Flex List Item block
- About
- What’s Inside this Block
- Block Availability
- Initial Block Setup
- Customizing the Block
  - Block Settings
- Pro Tips & Best Practices
- Common Questions
  - Can I customize the size of the heading?

The Flex List Item block creates visually distinctive list items with prominent numbering or markers. Perfect for rankings, collections, or featured content. Supports counting up, counting down, or unordered arrangements with full rich text, images, and links for each item.

The block includes a marker, a title, a content section, and a bottom border.

The marker can be a number (1, 2, 3), Roman numerals (I, II, III), or even an emoji ( 1️⃣, ?, ?).

The marker, title, and bottom border are optional.

The content section can include headings and paragraphs as well as various media and embeds.

This block is available on Posts and Pages.

The block contains placeholder content for the marker (01), title (Title), and content section (Subtitle and Summary).

The initial block toolbar options will show the options for the marker. As you navigate through the areas of the block the toolbar options will change.

The content section displays a heading and a paragraph, but you can include rich content, including media and embeds. Click into the content section and then delete the placeholders. Add your content using block inserter (+ plus sign).

The block can be customized through the block sidebar. Block settings affect the selected block only. They do not apply to all instances of the block.

Yes, you can adjust the size of the heading as well as its color. Use the block size bar to adjust the size.

Yes. Each Flex List Item block is independent, so you can insert ads, newsletter CTAs, and recommended post blocks between Flex List Item blocks.

Was this article helpful?

Thanks for the feedback!

---

## Images: Captions & Credits

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/images-captions-credits/

**Contents:**
- Images: Captions & Credits
  - Media Library
  - Article: Featured Image
  - Article: In-line Images

There is a lot of flexibility over how captions and credits display for article images on your Lede-platform site.

Images uploaded to your site (not added via URL) are stored in your Media Library. There are several metadata fields associated with every image which you can fill out in the Media Library:

The Featured Image on an Article is set in the Post Options when editing the Post/Article.

In-line images can be added throughout an Article via the Post Editor.

Was this article helpful?

Thanks for the feedback!

**Examples:**

Example 1 (unknown):
```unknown
If the information in the Caption and the Credit fields are identical, that information will not be duplicated on the frontend of the site.
```

---

## How to Embed PDFs

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/how-to-embed-pdfs/

**Contents:**
- How to Embed PDFs
- How to Embed Primary Source Documents via DocumentCloud
- Embedding Other PDFs via Google Drive or OneDrive
- Adjusting Height and Width Dimensions on Embed Codes

As a Lede publisher, there may come a time when you’d like to embed a PDF into one of your posts.

There are two recommended ways to do this, depending on the content of the PDF you’d like to embed.

DocumentCloud is a web-based software platform that helps you organize, research, annotate, analyze and publish primary source documents. It is free for journalism organizations.

To embed primary source documents through DocumentCloud:

If you want to embed a PDF that is not hosted by DocumentCloud, you can use either Google Drive or Microsoft OneDrive.

To embed other documents through Google Drive or OneDrive:

Google and Microsoft embeds use iframe code to display the embed on other sites.

The iframe code will include default height and width dimensions provided by the service used. Here are examples of codes for both services:

You can edit these dimensions by changing the width and height parameters in the iframe code.

The max width for any post content on the Lede platform is 720px (pixels), but we recommend using percentages to maintain scalability and accessibility across all devices.

Here is an example of this:

Below, we have changed the width of this iframe from 476px to 100% of the content width simply by changing the numbers inside of the double quotes for the width property from “476” to “100%”

You may also change the number for the height property (in pixels or percent), if desired. In our example below, we have changed the height to 600.

All of these numbers have been bolded in the code below for emphasis.

One important final note: Do not change or remove any other characters from this code block. If you do, the iframe will not render properly.

Original iframe code:

Updated iframe code (changed width and height):

Was this article helpful?

Thanks for the feedback!

---

## How to Use the Gallery Block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/how-to-use-the-gallery-block/

**Contents:**
- How to Use the Gallery Block
- How to add Gallery Blocks to a Post
- Gallery Block Options (in right sidebar unless otherwise specified)
- Image Block Options (in right sidebar unless otherwise specified)
- Styles: You can select from “Default” or “Rounded” for how each image displays in the gallery block.
- Note regarding legacy galleries

The “Gallery” Block is available on Lede v2 for use in your Posts.

To add a gallery in a post, insert (+) a Gallery block in the desired location and select images from the media library.

Once you have selected all desired images, click “Create a new gallery”, reorder the images if needed, and click “Insert gallery”. The editor will layout the gallery, making a best guess at the ideal layout based on the number of images selected, that you can then adjust.

Note: The gallery block inserts a “parent” gallery block which contains individual image blocks. You can adjust settings on the gallery block itself and on the individual image blocks. You can easily select the block you want to adjust in the Block List View.

Columns: You can adjust the number of columns for the gallery between one and three.

Crop Images: We recommend leaving this turned on.

Link to: Select either “None” or “Media file”. The “Media file” option creates a link to a standalone page that displays the image against a black background.

Note: The Attachment page option is not supported on the Lede platform.

Note: The Attachment page option is not supported on the Lede platform.

Image size: We recommend keeping this set to the default “Large” option so the images display as expected on the frontend.

Color – Background: You can change the background color which displays between images in a gallery.

Dimensions – Block Spacing: You can adjust the spacing between gallery images.

Note: The layout in the editor and how it displays on the frontend may not exactly match – Preview your post to see how the spacing will actually look.

Note: The layout in the editor and how it displays on the frontend may not exactly match – Preview your post to see how the spacing will actually look.

Alignment: (Not in sidebar) You can align the entire gallery in your post by clicking on the “Align” button for the block itself, and selecting your desired alignment.

Caption: (Not in sidebar) You can add a caption to the overall gallery by clicking on the “Add caption” button for the block itself (appears as “…” in a box), and adding a caption. The caption will display underneath the entire gallery.

Border: You can add a border to any image within the gallery block. The color of the border, along with the thickness can be adjusted, along with the border’s radius.

Caption: (Not in sidebar) A caption can be added to an individual image in two ways:

If a caption exists on the image in the Media Library it displays in the gallery automatically.

By selecting the image, clicking on the “Add caption” button (appears as “…” in a box), and adding a caption.

If your images are set to the “Default” style, the caption will display as an overlay at the bottom of the image. If your images are set to the “Rounded” style, the captiAon will display underneath the image.

If a caption exists on the image in the Media Library it displays in the gallery automatically.

By selecting the image, clicking on the “Add caption” button (appears as “…” in a box), and adding a caption.

If your images are set to the “Default” style, the caption will display as an overlay at the bottom of the image. If your images are set to the “Rounded” style, the captiAon will display underneath the image.

The appearance of legacy galleries (i.e. galleries that were migrated into your Lede v2 site from your previous site) depends on how the blocks were structured in the migration.

If your legacy galleries used the core WordPress gallery block, they will seamlessly convert to the expected Gallery display.

No action is required by you.

If your legacy galleries stored images outside of the actual gallery block, they will not be displayed as galleries.

You will need to manually update these legacy galleries, if desired.

If your legacy galleries used the core WordPress gallery block, they will seamlessly convert to the expected Gallery display.

No action is required by you.

No action is required by you.

If your legacy galleries stored images outside of the actual gallery block, they will not be displayed as galleries.

You will need to manually update these legacy galleries, if desired.

You will need to manually update these legacy galleries, if desired.

Was this article helpful?

Thanks for the feedback!

---

## Embeddable Forms forms for Contact Us pages, etc.

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/embeddable-forms-forms-for-contact-us-pages-etc/

**Contents:**
- Embeddable Forms forms for Contact Us pages, etc.
- JotForm
- Web3Forms

Embeddable forms provide a versatile solution for capturing user input directly on your site without requiring visitors to leave your page or open their email client. Common use cases include contact forms for general inquiries, user surveys, feedback collection, and support request management—all while keeping your team’s email addresses private and maintaining a streamlined user experience.

Many form builder embeds, such as Google Forms, can be inserted into a post or page using Lede’s iframe block.

Below are two free form solutions that may meet your needs. If you require a more custom solution, please file a support ticket with the details.

JotForm is a no-code form builder that enables you to create custom forms, surveys, registration forms, and application forms through a drag-and-drop interface. The free tier includes basic functionality with limitations on monthly submissions (100 responses) and form count (5 forms), and includes JotForm branding. Paid plans offer increased submission limits, unlimited forms, and the ability to remove JotForm branding. JotForm forms can be embedded using Lede’s iframe block.

Web3Forms is a lightweight, privacy-focused form service that processes form data rather than providing a visual form builder. Users integrate Web3Forms by adding a simple HTML form with a unique access key to their site. When visitors submit the form, Web3Forms processes the data and forwards it via email to specified recipients.

The free tier offers up to 250 submissions per month with unlimited forms and includes features like file uploads, spam filtering, and email notifications. Forms on the free tier include Web3Forms branding. Paid plans increase monthly submission limits and remove the Web3Forms branding. Since Web3Forms uses HTML rather than embeds, these forms can be added using the core WordPress HTML block.

If you need assistance implementing either of these solutions, please let us know.

Was this article helpful?

Thanks for the feedback!

---

## Featured Authors Block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/featured-authors-block/

**Contents:**
- Featured Authors Block
- Where It Can Be Used
- Configuration
  - Adding Authors
  - Reordering Authors
  - Adding a Title
  - Layout & Alignment
  - Appearance
- Examples
  - “Meet Our Team” Page

The Featured Authors block displays a curated grid of author cards on your site. Each card shows the author’s avatar (or their initials if no photo is set) and name, and links to that author’s archive page. You choose which authors appear and in what order, up to 12 per block.

This is useful for highlighting your team on an About page, showcasing contributors on a landing page, or featuring columnists on your homepage.

The Featured Authors block is available on Pages and Reusable Blocks only. It cannot be added directly to Posts.

If you want the block to appear on your homepage, add it to the page assigned as your site’s homepage, or include it via a reusable block.

Authors display in the exact order you select them. To change the order, use the up/down arrow buttons next to each author in the sidebar list. To remove an author, click the X button.

The block includes an optional title field above the author grid. Click the title area in the editor to type a heading. Basic formatting (bold and italic) is supported.

The grid is fully responsive:

Each author is displayed as a card containing:

Cards link to the author’s archive page, where readers can see all posts by that author.

The block respects your site’s color theme, including dark mode — no additional configuration is needed.

Add a Featured Authors block to your About or Team page with all your staff writers. Give it a title like “Our Writers” and use wide alignment to fill the page width.

Feature 4–8 of your most active or notable contributors on the homepage to give readers quick access to their favorite writers’ archives.

Create a reusable pattern containing a Featured Authors block with your core team. Insert it on multiple pages so it stays consistent and can be updated in one place.

Was this article helpful?

Thanks for the feedback!

---

## Affiliate Block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/affiliate-block/

**Contents:**
- Affiliate Block
- Affiliate Block
- Adding the block
- Field reference
- Working with the block
- A note on disclosure
- Common questions
- Examples
  - Dark Mode
  - Mobile

The Affiliate Block is a product card you can drop into a post to feature a single product with a buy link. It’s designed for reviews, gift guides, “best of” lists, and any article that recommends something readers might want to purchase.

The block ships with sensible defaults — the button reads “Buy on Amazon” until you change it — so you’ll have a working preview from the moment you insert it.

Pick a square or center-weighted image. The card uses a square crop. Album covers, book jackets, and centered product photography look great. For other shots, use the focal point control on the image to set what the crop should center on.

Write descriptive alt text. The standard WordPress alt text field on the image carries over — it helps with accessibility and image search.

Keep titles tight. Short, recognizable product names look best. If a product’s official name runs long (something like “The Land Is Inhospitable and So Are We”), it’s fine to trim it.

Use the subtitle for distinguishing details. “Vinyl LP,” “Hardcover,” “2024 edition,” “Refurbished” — anything that tells readers exactly what’s being linked.

Match the label to your editorial standards. “AFFILIATE” is the default and works for most uses. If you’d prefer “SPONSORED,” “PROMOTION,” or something custom, you can change the label text per block. Hide it entirely on posts that already carry a clear disclosure elsewhere.

Clear the CTA prefix for a cleaner button. Removing the “Buy on” prefix gives you a tighter button that just reads the retailer name and price — useful when you want the card to feel less promotional, or when the retailer name speaks for itself (“APPLE — $189”).

The “AFFILIATE” label on the card is a clear, visible signal to readers that the link is sponsored — which is exactly what disclosure guidelines (including the FTC’s in the US) ask for. Leaving the label on is the simplest way to handle disclosure for a single product mention.

For posts with several affiliate links, or for sites with a standing disclosure policy, you may prefer a written disclosure at the top or bottom of the article instead. In that case, you can hide the label on individual blocks. The disclosure itself remains your responsibility — the block supports your practice rather than replacing it.

Can I link to more than one retailer in a single block? Each block points to one retailer. To give readers a choice — say, Amazon and Bookshop — stack two Affiliate Blocks together.

Do prices update automatically? Prices are entered by hand and stay as written. For posts that will live a long time, you can use phrasing like “From $20” or “$28.99 at time of publication.”

How do I add click tracking or UTM parameters? Add them to the affiliate URL before pasting it in. Whatever you put in the Retailer URL field is exactly what readers will be sent to.

Can I add a star rating or pros/cons to the block? The block is intentionally a clean buy card — no ratings or review content inside. Put that content in the surrounding paragraphs, or pair the block with a dedicated review component.

What if the product image gets cropped in a way I don’t like? Open the image and adjust the focal point to set what the square crop should center on. If the photo really isn’t suited to a square crop, swap it for one that is.

Can I change “AFFILIATE” to something else, or remove it? Yes to both. Edit the label text in the block settings panel to rename it, or toggle it off to hide it.

Was this article helpful?

Thanks for the feedback!

---

## Recirculation block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/recirculation-block/

**Contents:**
- Recirculation block
- Recirculation Block
- Choosing which posts appear
- Layout and display
- Styling
- Common use cases
- Pro tips

The Recirculation block surfaces up to five related or recommended posts at the point where readers finish an article, giving them an easy next click and keeping them on your site. It lives in the Lede block category and replaces the styling of the older related-post block, so your existing related-post modules pick up the new card design automatically on deploy. No content migration is required, and editors don’t need to touch anything for the restyle to take effect.

At the top of every block sits a Recommended heading. This is a standard heading block, so you can rename it and adjust its font size, font family, color, and alignment using the normal heading controls.

Start by setting the number of posts you want to show, anywhere from one to five (the default is two). You then have two ways to fill those slots, and they work together:

If you pin some posts but don’t choose a fill term, or pin nothing at all, the empty slots fall back to the current article’s primary category automatically. This makes the block a reliable “set and forget” option for templated placements.

The block keeps itself clean as it fills:

The layout adapts to how many posts you’re showing:

If you’d rather keep images and the larger format even with three or more posts, turn on Keep full layout with 3+ posts.

Each card can display a featured image, an eyebrow (the primary category), the title, a byline, a timestamp, and a comment count. When a post has no featured image, the block falls back to the site’s default featured image. You can hide individual elements from the display panel using the Hide image, Hide eyebrow, Hide byline, Hide timestamp, and Hide comment count toggles.

Hide image acts as a master override and removes images in any layout. Since images only ever appear in the full layout, this toggle mainly matters for the one-to-two-post case or when you’ve turned on “Keep full layout with 3+ posts.”

Everything below is publisher-overridable and ships with sensible theme-token defaults:

The border control does double duty: it also styles the divider lines between posts. To remove those dividers, set the border width to 0 or the style to “none.” Item spacing tightens automatically when there are no images, so an image-free module reads as a clean, compact list.

In dark mode, background and text colors adapt on their own. Neutral preset backgrounds flatten to the dark surface and preset text drops to the base font color, but a custom hex text color you’ve deliberately chosen is left untouched.

Was this article helpful?

Thanks for the feedback!

---

## Custom Embed Block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/custom-embed-block/

**Contents:**
- Custom Embed Block
  - How to Create a Custom Embed Block
  - How to Insert a Custom Embed Block into a Post

The Custom Embed block allows you to securely embed certain types of iFrames that contain script tags in them, such as interactives from Tableau.

Note: You can insert more than one Custom Embed block in your post.

Was this article helpful?

Thanks for the feedback!

---

## Images: Art Direction with the Thumbnail Editor

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/images-art-direction-with-the-thumbnail-editor/

**Contents:**
- Images: Art Direction with the Thumbnail Editor

Lede uses a few different image aspect ratios throughout the site for different purposes. The aspect ratio of an image is the ratio of its width to its height, and is expressed with two numbers separated by a colon. So, for example, an image with a 16:9 aspect ratio that is 160 pixels in width would be 90px in height. We use these aspect ratios throughout Lede to ensure images load performantly—they don’t load more pixels than are necessary for the location in which they appear—and to ensure a pleasing and consistent layout on pages like the homepage.

In order to achieve a specific aspect ratio, however, images may be cropped in unexpected ways by our system resulting in people or text getting cut off in the image. In order to prevent this and give you full control over what appears in your images, we’ve built a tool for customizing (or art direct) the crop location of an image for each of the aspect ratios we use. This document will describe the aspect ratios we use on Lede and how to use the cropping tool, called the Thumbnail Editor.

Using the Thumbnail Editor

The thumbnail editor can be accessed from within the Media Library both on its standalone page and within the modal that opens when adding an image to a post within the post editor. To access it, select an image from the Media Library and scroll to the bottom of the right hand sidebar that appears. There is a “Show Thumbnails” button, as shown in the red square in the below screenshot:

After clicking this button, you should be presented with three options—one for each aspect ratio:

Select the aspect ratio for which you’d like to create a custom crop. Once you do so, it will send you to the editor. The editor will present you with a box that is locked to the selected aspect ratio. You can move and resize this box to display the portion of the image that you’d like users to see whenever that image appears at that aspect ratio.

Then click “Save Changes.” The updated crop will populate across the site.

Was this article helpful?

Thanks for the feedback!

---

## Essential WordPress Shortcuts for Content Creators

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/essential-wordpress-shortcuts-for-content-creators/

**Contents:**
- Essential WordPress Shortcuts for Content Creators
  - Essential WordPress keyboard shortcuts
  - To view all of the available shortcuts

Using keyboard shortcuts in the WordPress editor offers several practical benefits that can significantly improve your content creation workflow.

You can format text, insert elements, and navigate through content much faster than clicking through menus and toolbars. Simple actions like making text bold (Ctrl/Cmd + B) become nearly instantaneous.

They also help you keep your hands on the keyboard, which reduces the back and forth movement between keyboard and mouse, which can help prevent repetitive strain and feels more natural for many writers.

The WordPress editor includes shortcuts for everything from basic formatting to inserting specific blocks and duplicating content. Once you memorize the most common ones, you’ll find your content creation process becomes noticeably smoother and faster.

Ctrl/Cmd + B – Make selected text bold. This is probably the most frequently used formatting shortcut in any editor.

Ctrl/Cmd + K – Insert or edit a link. Super handy since linking is such a common task in web content, and it opens the link dialog instantly.

Ctrl/Cmd + Z – Undo your last action. Essential for quickly fixing mistakes or undoing accidental changes without losing your work.

/ (forward slash) – Opens the block inserter when you’re in an empty paragraph. This is unique to WordPress’s block editor and lets you quickly add any type of block by typing its name.

Ctrl/Cmd + Shift + D – Duplicate the current block. Perfect for when you want to create similar content blocks without starting from scratch.

Press Shift + Alt + H (or Shift + Option + H on Mac) to open the keyboard shortcuts help panel. This displays a comprehensive list of all available shortcuts organized by category.

You can also access this through the menu by clicking the three dots (More tools & options) in the top toolbar, then selecting Keyboard shortcuts from the dropdown menu.

Was this article helpful?

Thanks for the feedback!

---

## Shopify Blocks

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/shopify-blocks/

**Contents:**
- Shopify Blocks
- Shopify Blocks
- Connecting your store
- The Shopify Product block
  - Adding a product
  - Product settings
- The Shopify Collection block
  - Adding a collection
  - Collection settings
- Styling

If your site is connected to a Shopify store, two blocks let you feature your store’s merchandise directly inside posts and pages: the Shopify Product block, which showcases a single product, and the Shopify Collection block, which showcases a group of products. Both pull their content — image, title, and price — straight from your Shopify catalog, so you don’t re-type product details by hand. Prices and availability stay in sync with your store automatically.

Readers who click through are sent to your Shopify storefront — either to the product page or, optionally, straight to a pre-filled cart.

The Shopify blocks appear once your store is connected, and you can set this up yourself — no need to contact support. Open the Shopify tab in your Publisher App settings and fill in:

Save your settings, and the Shopify Product and Shopify Collection blocks become available in the editor.

Use this block to spotlight one item — a featured release, a recommended product in a review, or a single piece of merch tied to a story.

Use this block to feature a group of products — a seasonal line, a category, or a curated set you’ve built as a collection in Shopify. It can display either the collection’s cover image or the individual products inside it.

Both blocks share a Styling panel in the block settings. By design, every option draws from your site’s existing brand styles, so the blocks always match the rest of your site. You’re choosing from your theme’s fonts, sizes, spacing, and colors rather than picking arbitrary values — there’s no way to set an off-brand color or font here.

Every control defaults to blank, which means “use the brand default.” You only need to touch these when you want a specific block to look different from the standard.

Unlike a manually entered product card, the Shopify blocks keep themselves current. When the page loads, the blocks check your Shopify store for the latest price and stock status, so what readers see matches your storefront. This refresh is cached for a few minutes, so changes you make in Shopify appear on the site shortly after — not necessarily the very instant you save.

When a product sells out, the block shows a Sold out label and the button stops offering “add to cart” — instead it simply links to the product page. You don’t have to edit the post; out-of-stock items are handled for you.

I don’t see the Shopify blocks in the editor. Make sure your store is connected: open the Shopify tab in your Publisher App settings and confirm your Storefront API token and store hostname are filled in. A common mistake is including http:// or https:// in the store hostname — remove it so the field holds just the hostname (for example your-store.myshopify.com).

Do I need to set a Store URL? Only if your public storefront lives somewhere other than your store hostname. Leave it blank and readers are sent to your store hostname by default; set it to a custom domain if your shop is published there.

Do I need to update prices by hand? No. Prices and stock status are pulled from Shopify automatically and refresh on their own. The price captured when you inserted the block is only a fallback for the brief moment before the live value loads.

What happens when something goes out of stock? The block automatically shows a “Sold out” label and the button changes to a plain link to the product page. No edit needed.

Can the button add an item straight to the cart? Yes. Set the call to action to the cart option, and the button sends readers to your storefront with the item already in their cart.

What’s the difference between the cover image and individual products in a Collection? Cover image shows the single image you’ve set on the collection in Shopify — a clean, magazine-style promo that links to the full collection. Individual products shows a grid of the actual items, each with its own image, price, and button.

Will the blocks match my site’s design? Yes. They use your site’s existing fonts, colors, and spacing by default. The Styling panel only lets you choose from your established brand styles, so the blocks can’t look off-brand.

Can I show more than one product without a collection? Yes — add multiple Shopify Product blocks, or use a Shopify Collection block in individual-products mode if the items already live in a Shopify collection.

Was this article helpful?

Thanks for the feedback!

---

## The Contact Us Form block

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/the-contact-us-form-block/

**Contents:**
- The Contact Us Form block
- Form Appearance
- Before You Begin
- Setup Instructions
  - Step 1: Obtain Web3Forms Access Key(s)
  - Step 2: Add the Contact Us Form Block
  - Step 3: Configure Your Form
    - Single Destination Setup
    - Multi-Department Setup
  - Step 4: Customize Your Page (Optional)

The Contact Us Form block is a custom block that integrates Web3Forms to display a contact form directly on any post or page of your website. This seamless integration provides a professional contact solution without visible third-party branding. It is fully responsive and automatically adapts to light and dark mode. A key feature of the Contact Us Form block is that is supports multiple destinations / departments. You can use a single form for editorial tips, ad inquiries, bug reports, etc.

Consider whether the Contact Us Form block meets your needs:

The form provides a general text field for messages rather than customizable specific fields.

Your configuration depends on whether you need a single destination or multiple departments:

For a general contact form with one recipient:

For forms that route to different departments (e.g., Sales, Support, Editorial):

Since the Contact Us Form is a standard block, you can:

The form becomes active immediately upon publishing—no additional activation steps required.

Was this article helpful?

Thanks for the feedback!

---

## Homepage Recipe: Left Bleed Sidebar with Menu

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/homepage-recipe-left-bleed-sidebar-with-menu/

**Contents:**
- Homepage Recipe: Left Bleed Sidebar with Menu
- Prerequisites
- Step 1: Set Up the Page Layout
- Step 2: Prepare the Columns
- Step 3: Create the Left Bleed Container
- Step 4: Add the Navigation Menu
- Best Practices

Before beginning, create the menu you want to display on the homepage. (Detailed menu creation instructions.) Choose a brief, descriptive name for the menu, as this will be visible to users.

The left bleed container should now appear in your editor with the selected background color.

Note: The menu title will not display in the editor but will be visible in the preview and on the frontend.

By following these steps, you’ll create an eye-catching left bleed sidebar that enhances your homepage!

Was this article helpful?

Thanks for the feedback!

---

## Post Templates

**URL:** https://docs.joinlede.com/creating-content-wordpress-admin/post-templates/

**Contents:**
- Post Templates
  - Create a New Template
  - Set an Alternate Template for a Post
  - Manage Templates
    - Edit a Template
    - Remove a Template

Learn how to set up post templates on the Lede platform to help streamline your editorial process. Post templates are great to use if you find yourself often (or always) inserting the same block in the same location (beginning and/or the end) of your posts.

You can also have alternate templates which apply to only a subset of your posts.

To manage your templates, navigate to Posts > Templates.

Was this article helpful?

Thanks for the feedback!

---
