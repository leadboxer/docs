# ActiveCampaign

Step 1: Track email opens

To track mail open/reads from your Active Campaign audience in LeadBoxer, you need to add a LeadBoxer tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. Go to your campaign or template
2.  Add an HTML element in where we can add our tracking pixel

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/61deaad91adf855680c78f5b/file-3uixi9QVzq.png" alt=""><figcaption></figcaption></figure>
3. paste in your email tracking pixel at the bottom of the HTML:

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=my-campaign&email=%EMAIL%">
```
{% endcode %}

Close and Save

Notes:

* Don't forget to change the DATASET ID to your own
* Change the campaign value to reflect the email title or campaign name&#x20;
* you can add other template variables as parameters if you have them, eg&#x20;

```
&firstName=%FIRSTNAME%
```

### Step 2: Track email clicks and identify prospects on your site

To track email clicks, you need to modify the links inside your email campaigns and add this parameter to the URL of the link:

**?email=%EMAIL%**

This will allow us to identify the individual visitors when they land on your site.

Optionally but recommended, you should add additional parameters to enrich the visitor with other information from your database:

**example URL**

{% code overflow="wrap" %}
```url
https://www.YOURDOMAINNAME.com/my-landing-page/?firstName=%FIRSTNAME%&lastName=%LASTNAME%&email=%EMAIL%&companyName=%COMPANYNAME%
```
{% endcode %}

Tip: Best practice is to test before sending out a mass email



To see more on For more details see these pages:

[https://help.activecampaign.com/hc/en-us/articles/220709307-Personalization-Tags#ways-to-use-personalization-tags-1](https://help.activecampaign.com/hc/en-us/articles/220709307-Personalization-Tags#ways-to-use-personalization-tags-1)
