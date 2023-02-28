---
description: How to track email opens and clickthroughs from Woodpecker
---

# Woodpecker

To track mail open/reads, you need to add the tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. go to your drip campaign or template
2. edit your campaign or template and switch to HTML (\</>)
3. paste in your email tracking pixel at the bottom

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=woodpecker&email={{EMAIL}}&firstName={{FIRST_NAME}}&lastName={{LAST_NAME}}&company={{COMPANY}}" width="1" height="1" >
```
{% endcode %}

**Notes:**

* Change datasetId to reflect yours
* Optionally, change the campaign value to reflect the email title or campaign name&#x20;
* you can add other snippets variables as parameters if you have them

### Track clicks and identify prospects on your site

To track email clicks, you need to modify your links to include these parameters&#x20;

example URL

{% code overflow="wrap" %}
```url
https://www.YOURDOMAINNAME.com?email={{EMAIL}}&companyName={{COMPANY}}
```
{% endcode %}



For more details see this page:\
[https://woodpecker.co/help/use-custom-fields-snippets/](https://woodpecker.co/help/use-custom-fields-snippets/)\


