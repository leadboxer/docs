# QuickMail

This tutorial tells you how to get setup for LeadBoxer email tracking of recipients originating from your QuickMail emails.

LeadBoxer will show you the email of the person who clicked through the email, simply by a) adding a special link in the emails sent and b) adding code to the landing page.

Technical requirements:

1. LeadBoxer account
2. QuickMail account

Steps:

1. Customize the links in your email newsletter
2. Install the email tracking pixel

Assuming you fulfilled both requirements, let's proceed to step 1.

### Step 1

Capturing data from your email readers involves a small change to your normal workflow.

Create your emails like you always do, and make sure you add a link to a landing page. The landing pages will automatically capture the information being sent from the QuickMail email once they click a link.

When your email is ready, for each link that goes to your website, you need to add custom parameters to your link. These parameters, in QuickMail known as 'Attributes', and you need to add look like this:

```
?email={{prospect.email}}
```

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/615ade880754e74465f162aa/file-h1QUlefUtd.png)

This appends the email address to the url of the landing page and we will use this to identify the prospect on the site.

**TIP:** You can do this for all fields available in QuickMail eg:

```
?email={{prospect.email}}&firstName={{prospect.first_name}}&lastName={{prospect.last_name}}&companyName={{company.name}}
```

**Tip 2**\
add UTM tags to get these clicks also identified in your Analytics solution like Google Analytics

```
?email={{prospect.email}}&firstName={{prospect.first_name}}&lastName={{prospect.last_name}}&companyName={{company.name}&utm_medium=email&utm_source=quickmail&utm_campaign=email1
```

Save your email, and test the links by hovering on them in the preview version, you should see the email address and other fields appended to the url on your landing page. The following image shows what you should see appended to the url of your landing page:

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/615474a600c03d672075badf/file-S9d2KyFeoH.png)

### Step 2

Next, you will need to add the LeadBoxer email tracking pixel so that we can also track email opens and get information on how often customers read your emails.

You can add this email tracking pixel to the source of your email by clicking the 'img' feature in the editor

Here is the link of the tracking pixel you need to paste in.&#x20;

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/615ae258e5648623c88e130f/file-H8ZexUwQFD.png" alt=""><figcaption></figcaption></figure>

**Tip**: Construct yours in a plain text before you start

```
https://track.leadboxer.com/log?datasetId=yourDatasetId&campaign=YourCampaignName&email={{prospect.email}}
```

Do not forget to replace the  **yourDatasetId** and **YourCampaignName** with your own values.

From there on LeadBoxer will take over and add the data to the lead. Obviously the LeadBoxer pixel needs to be installed on the pages they land on.&#x20;

It's always a good idea to test this thoroughly before sending this to you main lists.&#x20;

If things are working, you can now see who is actually interested in your emails and what products or services.
