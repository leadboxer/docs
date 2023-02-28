---
description: How to track email opens and clickthroughs from Lemlist emails
---

# Lemlist

### Step 1: Track email opens

To track mail open/reads, you need to add the tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. go to your drip campaign or template
2. edit your campaign or template and switch to HTML (\</>)
3. paste in your email tracking pixel at the bottom

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=lemlist&email={{email}}&firstName={{firstName}}&lastName={{lastName}}&company={{companyName}}" width="1" height="1" >
```
{% endcode %}

{% hint style="info" %}
**Notes:**

* Change datasetId to reflect yours
* Optionally, change the campaign value to reflect the email title or campaign name&#x20;
* you can add other custom variables as parameters if you have them
{% endhint %}

### Step 2: Track clicks and identify prospects on your site

To track email clicks, you need to modify your links to include these parameters&#x20;

example URL

{% code overflow="wrap" %}
```url
https://www.YOURDOMAINNAME.com?email={{email}}&companyName={{companyName}}
```
{% endcode %}



For more details see this page:

[https://help.lemlist.com/en/articles/4452688-custom-variable-format](https://help.lemlist.com/en/articles/4452688-custom-variable-format)\


