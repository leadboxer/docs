# dotdigital

### Identify & track dotdigital email recipients on your website&#x20;

#### Step 1: Track email opens

To track mail open/reads from your dotdigital audience in LeadBoxer, you need to add a LeadBoxer tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. Go to your campaign or template
2. Create or edit an element in where we can add our tracking pixel, usually a footer element or similar.
3. switch to HTML view, so you can ad HTML code (\</>)![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fd379c83d1d2a5b1c5e9d44/file-tiO8VDf4iL.png)
4. paste in your email tracking pixel at the bottom of the HTML:

```
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign={{ campaign.name }}&email={{ contact.data.email }}&firstName={{ contact.data.firstname }}&lastName={{ contact.data.lastname }}">
```

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fd37afac868cb6df3a80bf3/file-HslM0oZO0X.png)

Close and Save

**Notes:**

* Don't forget to change the DATASET ID to your own&#x20;
* You can add other data fields variables as parameters by simply adding these to the pixel, eg \&companyName=\{{ contact.data.company \}}
* For more details on advanced data fields in dotdigital see: [https://support.dotdigital.com/hc/en-gb/articles/360000044424-Advanced-personalisation-an-overview](https://support.dotdigital.com/hc/en-gb/articles/360000044424-Advanced-personalisation-an-overview)

#### Step 2: Track email clicks and identify prospects on your site

To track email clicks, you need to modify the links inside your email campaigns and add this parameter to the URL of the link:

In dotdigital, this can be done automatically with the advanced feature called Link tracking.

1. FIrst make sure you have the Google Analytics tracking enambled![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fd37cebc868cb6df3a80c02/file-LauJL1O9gk.png)
2. Then add your parameters to the list. You can add multiple parameters but **email** is required. use @EMAIL@ as value![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fd37ed63d1d2a5b1c5e9d69/file-DkNSvxFjU7.png)

This will allow us to identify the individual visitors when they land on your site.

Optionally but recommended, you can add additional parameters to enrich the visitor with other information from your database.

For more details see these pages from the dotdigital documentation: [https://support.dotdigital.com/hc/en-gb/articles/115001298084-Add-tracking-to-email-campaign-links](https://support.dotdigital.com/hc/en-gb/articles/115001298084-Add-tracking-to-email-campaign-links)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on December 11, 2020
