# HubSpot

{% hint style="info" %}
Make sure you also enable our [HubSpot Integration](../../other/hubspot.md), as this will sync all your existing contacts with LeadBoxer and allow you to enrich your HubSpot contacts with LeadBoxers rich firmographic and marketing data.
{% endhint %}

Tracking HubSpot marketing emails is easy.U

To track email open events, either add this tracking image to your template as a piece of HTML

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR_DATSET_ID&campaign=Newsletter&email={{contact.email}}"/>
```
{% endcode %}

Alternatively, you can add an image from an URL  like this:

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5d9f34c22c7d3a7e9ae25805/file-Z3n5jih2z8.png) ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5d9f352f2c7d3a7e9ae2581d/file-AheGf4jI5H.png)

***

Make sure you enable the HubSpot integration so we can connect your HubSpot contacts with LeadBoxer leads.

See instructions here:[https://help.leadboxer.com/leadboxer/integrations/other/hubspot](https://help.leadboxer.com/leadboxer/integrations/other/hubspot)&#x20;

Optionally, you can also identify your HubSpot contacts using merge tags on the links to your site.

To track link clicks and identify these readers on our site you need to be appended with a parameter like in this example:

{% code overflow="wrap" %}
```url
https://www.leadboxer.com/?email={{contact.email}}&firstName={{contact.firstname}}&lastName={{contact.lastname}}&companyName={{company.name}}
```
{% endcode %}

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5d9f372404286364bc903d64/file-NstHPmk2UM.png)
