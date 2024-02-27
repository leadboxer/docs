---
description: How to track email opens and clickthroughs from instantly.ai
---

# Instantly

To track mail open/reads, you need to add the tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding a tracking pixel:

1. go to your campaigns
2. edit your campaign or template and switch to HTML (< >)
3. paste in your email tracking pixel at the bottom

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=woodpecker&email={{email}}&firstName={{firstName}}&lastName={{lastName}}&company={{company}}" width="1" height="1" >
```
{% endcode %}

**Important: You will need to customize above code:**

* Change datasetId to reflect yours
* Change the campaign value to reflect the email title or campaign name&#x20;
* you can add other custom variables as parameters if you have them

### Track clicks and identify prospects on your site

To track email clicks, you need to append the links to your site and to include these parameters&#x20;

```html
?email={{email}}
```

Tip: You can also add other custom fields as parameters

example URL

{% code overflow="wrap" %}
```url
https://www.yourdomain.com?email={{email}}&companyName={{companyName}}
```
{% endcode %}



For more details see this page:\
[https://help.instantly.ai/en/articles/6135930-how-to-add-variables](https://help.instantly.ai/en/articles/6135930-how-to-add-variables)\


