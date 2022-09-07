# Reply.io email tracking

This tutorial tells you how to get setup for LeadBoxer email tracking of recipients originating from your Reply.io emails.

LeadBoxer will show you the email of the person who clicked through the email, simply by a) adding a special link in the emails sent and b) adding code to the landing page.

Technical requirements:

1. LeadBoxer account
2. Reply.io account

Steps:

1. Customize the links in your email newsletter
2. Install the email tracking pixel

Assuming you fulfilled both requirements, let's proceed to step 1.

### Step 1

Capturing data from your email readers involves a small change to your normal workflow.

Create your emails like you always do, and make sure you add a link to a landing page. The landing pages will automatically capture the information being sent from the Reply.io email once they click a link.

When your email is ready, add custom parameters to your link. These parameters, known as ' [merge tags](http://mailchimp.com/features/merge-tags/)', will be added to your links:

```
?email={Email}
```

this appends the email address to the url of the landing page. You can do this for all fields available in Reply.io eg:

```
?email={Email}&firstName={firstName}&lastName={lastName}&companyName={company}
```

Save your email, and test the links by clicking on them in the final draft, you should see the email address and other fields appended to the url on your landing page. The following image shows what you should see appended to the url of your landing page:

[![Mailchimp-LeadBoxer-landing-url](https://www.leadboxer.com/wp-content/uploads/2015/02/Mailchimp-LeadBoxer-landing-url.png)](https://www.leadboxer.com/wp-content/uploads/2015/02/Mailchimp-LeadBoxer-landing-url.png)

### Step 2

Next, you will need to add the LeadBoxer email tracking pixel so that we can also track email opens and get information on how often customers read your emails.

You will need to add this email tracking pixel to the source of your email or templates, place it at the bottom of the source.

```
<img src="https://track.leadboxer.com/log?datasetId={{yourDatasetId}}&campaign={{YourCampaignName}}&email={Email}&firstName={firstName}&lastName={lastName}&companyName={company}">
```

![](https://downloads.intercomcdn.com/i/o/29561275/7217a68d6af946526de3eac5/Material\_2016-08-26\_06-47-11.png)

Do not forget to replace the  **yourDatasetId** and **YourCampaignName** with your own values.

From there on LeadBoxer will take over and add the data to the lead. Obviously the LeadBoxer pixel needs to be installed on the pages they land on.&#x20;

It's always a good idea to test this thoroughly before sending this to you main lists. If things are working, you'll see the emails of leads interested in your newsletter's landing page.

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on October 4, 2021
