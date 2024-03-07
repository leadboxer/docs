---
description: How to track email opens and clickthroughs from mailerlite.com
---

# Mailerlite

To track mail open/reads, you need to add the tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding a tracking pixel:

1. go to your campaigns
2. edit your campaign content or template&#x20;
3. Add a 'code' block at the bottom of your email&#x20;
4. paste in your email tracking pixel at the&#x20;

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=MY-DATASET_ID&campaign=test&email={$email}"/>
```
{% endcode %}

**Important: You will need to customize above code:**

* Change datasetId to reflect yours
* Change the `campaign` value to reflect the email title or campaign name&#x20;
* you can add other custom variables as parameters (eg \&firstName={$first\_name} if you have them

### Track clicks and identify prospects on your site

To track email clicks, you need to append the links to your site and to include these parameters&#x20;

```html
?email={$email}
```

Tip: You can also add other custom fields as parameters

example URL

{% code overflow="wrap" %}
```url
https://www.yourdomain.com?email={$email}&companyName={{companyName}}
```
{% endcode %}



For more details see this page:\
\
[https://www.mailerlite.com/help/how-to-create-and-use-custom-fields](https://www.mailerlite.com/help/how-to-create-and-use-custom-fields)



