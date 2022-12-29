# 🛠 Getting Started

In this document you will find the essential steps needed to get the most out of your leadBoxer (trial) account. Not all steps are required, however we encourage you to complete as many steps as possible.

### Track website behaviour

In order to get going, there is one essential step to take.&#x20;

Even though this step is simple (takes less than 5 minutes) it’s the most important step of all, if you ever want to see any results during your trial.

The tracking code (aka Lead Pixel) is what makes it possible for us to track your website visitors, so without the pixel, we will not be able to track anything - meaning no new leads 😉

Once the Lead Pixel is installed on your site we will start collecting data and provide more information about the companies and organisations that visit your site.

Use any of the following plugins or tutorials to get started:&#x20;

* [Wordpress](integrations/website/wordpress-plug-in/)
* [Drupal](integrations/website/drupal-module.md)
* [Google Tag Manager](integrations/website/google-tag-manager-gtm.md)

If you do not use any of the above solutions, simply paste your pixel code into the source code of your website just before the end tag.

You can find your tracking code / lead-pixel on your welcome screen or in the dataset overview.

You can also send your lead pixel to your developer or the agency responsible for your site from within your dashboard.

***

### Track Marketing / Newsletter emails

To track email behaviour and combine this information with visitor website activity, we offer solutions for almost all major email providers.

NOTE: LeadBoxer Email Tracking consists of 2 separate elements. Meaning there are two steps needed to get everything setup:

Tracking email opens and clicks Identifying leads and customers by name when they visit your website.&#x20;

Top integrations/ tutorials:

* [Mailchimp](integrations/email/marketing-emails/mailchimp.md)
* [Sharpspring](integrations/email/marketing-emails/sharpspring.md)
* [Copernica](integrations/email/marketing-emails/copernica.md)
* [Intercom](integrations/email/marketing-emails/intercom-email-tracking.md)
* [Reply.io ](integrations/email/marketing-emails/reply.io.md)
* [Poppulo](integrations/email/marketing-emails/poppulo.md)
* [Spotler](integrations/email/marketing-emails/spotler.md)
* [See all... ](integrations/email/marketing-emails/)

**For all other email / marketing automation providers**

To track email clicks and combine this information with visitor website behaviour, the links in your emails need to be customized with ‘merge tags’. ( [documentation](integrations/email/marketing-emails/intro-track-contacts-on-your-site.md))

To measure email opens, a pixel specific to email tracking needs to be implemented. [Documentation can be found here.](integrations/email/marketing-emails/intro-track-email-opens.md)

***

### Track individual email behaviour

Description: Track all of your individual emails that you send from your mail client&#x20;

* [Gmail](integrations/email/individual-emails/github-integration.md) &#x20;
* [G Suite](integrations/email/individual-emails/g-suite-email-tracking.md)
* [Office 365 / Outlook 365](integrations/email/individual-emails/official-outlook-add-in.md)
* [Manually](integrations/email/individual-emails/manually-identify-leads-using-email.md)

***

### LinkedIn - Track and identify Leads

To See how LeadBoxer and LinkedIn can work together see this overview:

[Best LinkedIn Strategies using LeadBoxer](integrations/for-support/linkedin.md)

***

### Capture marketing & campaign data

Consider using UTM tags - parameters for your next paid traffic campaign (if you do not already)&#x20;

LeadBoxer automatically captures Google Analytics tracking tags (UTM tags) and adds campaign data to your leads or customers. We do this by automatically capturing the utm\_\* parameters from the landing pages and adding the UTM values to each lead profile.&#x20;

In order to take full advantage of this feature, make sure that all your online ads, links in your newsletters or emails, social posts, etc are tagged properly with these links.

More information can be found here: [All about UTM tags](integrations/website/tracking-marketing-campaign-data-utm-tags.md)

***

### Track your other customer touch-points

In order to take full advantage of our platform, we strongly recommend that you implement our identification & enrichment methods on as many touch-points as possible. Touch points are all the places where your leads or customers digitally interact with your company and provide (personal) information:

#### - Contact forms

We provide 2 ways to track forms.&#x20;

* [Automatic form tracking](integrations/website/automatic-form-tracking.md) for simple forms
* [Manual form tracking](integrations/website/manual-form-tracking.md) for complex or custom forms
* [Gravity Forms Plugin](integrations/website/gravity-form-tracking.md)

#### - Newsletter signup

The process of tracking your newsletter sign-ups is similar to the technology used to track forms; you can make use of automatic or manual form tracking. Once in the system, all behaviour (activity) will be captured.

#### - White-paper downloads&#x20;

Similar to contact forms, you can use both ways of form tracking, but we also provide the technology to use a ‘download with LinkedIn’ button so that your leads identify themselves by providing LinkedIn credentials.&#x20;

#### - Logins

If you have a section on your site where users or customers login, this is a perfect place to identify them. Tracking logins delivers numerous benefits - it let’s you see and associate your clients and users within your system and makes you aware of what they are doing. Very importantly it allows for audience segmentation, meaning we can exclude logins from your lead list.

***

### Third party enrichment

We will try to enrich your leads with as much firmographic information as we possibly can. However you might find the need to add some additional sources in order to increase the enrichment rates or you might need specific data-fields we do not provide out o the box.

* Clearbit&#x20;
* [Google places](integrations/for-support/google-places.md)

### Bring your own data (custom enrichment)

If you have other data that you would like to combine or collect, we have an open API that can be used to accomplish this:&#x20;

* [Enriching customer profile data ](fundamentals/elements/enrichment.md)
* [Tracking custom behavioral touchpoints (events)](integrations/website/lead-tracking-pixel.md#what-are-events)

***

### Set your Leadscore

Lead Scoring is a powerful concept making its way to the top of everyone’s mind in the Lead Generation space. Now that you are collecting data, it’s time to set custom, automatically calculated lead scoring.

Once you start using LeadBoxer, you'll notice that every lead has a Leadscore. By default, your leads are sorted based on a standard Leadscore setting. Now is the time to give it your personal touch. If you are unsure how to start, you can select one of our predefined settings, and adjust them based on your needs. To do this, just go to the leadscore page.

[Learn how to change the leadscore](guides/how-to-set-your-leadscore.md)

***

#### Create your segments

In Leadboxer, you can create segments. A segment is basically a saved set of filters on your data. Very easy to use always accessible from drop-downs. You can save segments, edit or duplicate them, or even send scheduled emails containing your segment results.

LeadBoxer contains 1 default segment: Top leads and is used to send you your daily or weekly notification. You can modify this segments or create your own.

[Learn how to use filters and create segments](guides/creating-your-first-segment.md)

***

### Setup notifications

Once you have defined your Segment(s), you can have them emailed to yourself and/or colleagues on a daily or weekly basis, in html, PDF or .csv formatting.

A good practice is to create Segments for your key accounts, or geographical sales-team regions – get notified when your site(s) are visited by your top prospects, customers or account based targets.

[Learn how to setup notifications](guides/how-to-create-a-notification.md)

***

### Add all your sales and marketing colleagues

Getting the data to the right people within your organisation is mission-critical. Therefore we recommend adding colleagues and managers. With LeadBoxer you can add users and set individual access permissions.

See a tutorial [here](https://docs.leadboxer.com/article/70-how-to-add-a-user-to-your-account)

You can add a users in your [users overview](guides/how-to-add-a-user.md)

***

### Measure all your websites

Some organisations have more than one website, LeadBoxer allows you to add multiple sites to your account, for example a specific product, region, language or event.

For a detailed tutorial to add a site see [here](guides/how-to-add-a-datasets.md)

Simply add them to your account in the [dataset overview](https://app.leadboxer.com/datasets) and you will receive a unique lead pixel to install on these domains.

We also offer cross-domain tracking, please contact us for details and pricing.

***

### Integrate with Zapier

LeadBoxer offers a free Zapier integration so that you can use LeadBoxer data with almost any of your favourite software and sales tools without being a developer.

This means you can set up a LeadBoxer account, collect leads, and send them where they need to go. For example; integration with SalesForce. LeadBoxer will work to identify leads on your site and feed them into your SalesForce CRM, so that they are visible to your sales team.

Get started with [LeadBoxer on Zapier](integrations/website/how-to-get-started-with-leadboxer-on-zapier.md)

***

### Integrate with your CRM

Measure complete engagement; logins, website visits, emails opens, etc, and automatically

submit lead activity into your CRM.

### - Pipedrive

Pipedrive is a sales driven CRM and Lead management tool designed to help sales teams manage intricate or lengthy sales processes. We have built a direct integration for this fantastic Sales tool. For more details see our [Pipedrive documentation](integrations/other/pipedrive/)

#### - Other CRM's

For other CRM vendors you can use [Zapier App](integrations/website/how-to-get-started-with-leadboxer-on-zapier.md) or our [API](https://docs.leadboxer.com/collection/109-api) to roll your own

***

#### Dashboarding

[Whatagraph Integration](broken-reference)
