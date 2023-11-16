# Autopilot

### Step 1: Track email opens

To track mail open/reads from your Autopilot audience in LeadBoxer, you need to add a LeadBoxer tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. Go to your campaign or template
2.  Add or edit an HTML element in where we can add our tracking pixel

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5e72342004286364bc96e092/file-nZflR7AMcN.png" alt=""><figcaption></figcaption></figure>
3. Add in your email tracking pixel at the bottom of the HTML:

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=Autopliot-email-1&email={{person.email}}" width="1" height="1">
```
{% endcode %}

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5e7233e42c7d3a7e9ae95e5d/file-18vPgMVFXe.png)

Close and Save

**Notes:**

* Don't forget to change the **DATASET ID** in the pixel to your own
* Change the campaign value to reflect the email title or campaign name&#x20;
* you can add other template variables as parameters if you have them, eg&#x20;
  * _\&companyName=\{{person.organization\}}_
  * _firstName=_\{{person.firstname\}}
  * etc



### Step 2: Track email clicks and identify prospects on your site

To track email clicks, you need to modify the links inside your email campaigns and add this parameter to the URL of the link:

**\&email=\{{person.email\}}**

This will allow us to identify the individual visitors when they land on your site.

**UTM tags**\
In order for us to classify this visit coming an email, you need to add the UTM tag **\&utm\_medium=email**\
So either enable the automatic UTM tag settings in Autopilot or manually add these to your links

Optionally but recommended, you should add additional parameters to update the visitor with other information from your database:

**Full example URL**

{% code overflow="wrap" %}
```
https://www.YOURDOMAINNAME.com/my-landing-page/?firstName={{person.firstname}}&lastName={{person.lastname}}&email={{person.email}}&companyName={{person.organization}}&utm_medium=email
```
{% endcode %}

Tip: Best practice is to test before sending out a mass email
