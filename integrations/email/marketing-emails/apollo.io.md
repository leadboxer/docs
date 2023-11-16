# Apollo.io

### Identify & track Apollo email recipients on your website&#x20;

#### Step 1: Track email opens

To track mail open/reads from your Apollo audience in LeadBoxer, you need to add a LeadBoxer tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. Go to your campaign or template
2. Create or edit an element where we can add our tracking pixel, usually a footer element or similar.
3.  Switch to HTML view, so you can ad HTML code (\</>)

    <figure><img src="../../../.gitbook/assets/Cursor (1).png" alt=""><figcaption></figcaption></figure>
4. Paste your email tracking pixel into the bottom of the HTML:

{% code overflow="wrap" %}
```html
<div><img src="https://track.leadboxer.com/log?datasetId=YOUR-DATASET-ID&campaign=Apollo-outreach-email-day-01&email={{email}}&firstName={{first_name}}&lastName={{last_name}}&companyName={{company}}"></div>
```
{% endcode %}

5. Save

**Notes:**

* Don't forget to change the DATASET ID to your own.&#x20;
* You can add additional data fields variables as parameters by simply adding these to the pixel, eg \&companyName=\{{ contact.data.company \}}
* For more details on advanced data fields in Apollo see:&#x20;
* [https://knowledge.apollo.io/hc/en-us/articles/4409415084813-Use-Basic-Dynamic-Variables#toc\_3](https://knowledge.apollo.io/hc/en-us/articles/4409415084813-Use-Basic-Dynamic-Variables#toc\_3)

### Step 2: Track email clicks (click-thrus) and identify prospects on your site

To track email clicks, you need to modify the links inside your email campaigns and add this parameter to the URL of the link:

**\&email=\{{email\}}**

This will allow us to identify the individual visitors when they land on your site.



<figure><img src="../../../.gitbook/assets/Cursor (2).png" alt=""><figcaption></figcaption></figure>

Optional, but recommended; add additional parameters to enrich  visitors with additional information from your database:

**example URL**

{% code overflow="wrap" %}
```url
https://www.YOURDOMAINNAME.com/my-landing-page/?firstName={{first_name}}&lastName={{last_name}}&email={{email}}&companyName={{company}}
```
{% endcode %}

NOTE: remember to update 'YOURDOMAINNAME' with your url.\
Tip: Best practice is to test before sending out a mass email
