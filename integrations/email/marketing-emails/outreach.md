# Outreach

### Step 1: Track email opens

To track mail open/reads from your Outreach audience in LeadBoxer, you need to add a LeadBoxer tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. Go to your campaign or template
2. Create or edit an element in where we can add our tracking pixel, usually a footer element or similar.
3. switch to HTML view, so you can ad HTML code (\</>)
4. paste in your email tracking pixel at the bottom of the HTML:

```
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=outreach&email={{email}}" width="1" height="1">
```

Close and Save

Notes:

* Don't forget to change the DATASET ID to your own
* Change the campaign parameter value to reflect the email title or campaign name&#x20;
* you can add other template variables as parameters if you have them, eg _\&companyName={$companyName}_\


***

### Step 2: Track email clicks and identify prospects on your site

To track email clicks, you need to modify the links inside your email campaigns and add this parameter to the URL of the link:

**\&email=\{{email\}}**

This will allow us to identify the individual visitors when they land on your site.

Optionally but recommended, you should add additional parameters to enrich the visitor with other information from your database:

**example URL**

```
https://www.YOURDOMAINNAME.com/my-landing-page/?firstName={{first_name}}&lastName={{last_name}}&email={{email}}&companyName={{company}}
```

Tip: Best practice is to test before sending out a mass email

***

To see more on For more details see these pages:

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on August 11, 2022
