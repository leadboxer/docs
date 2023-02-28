# Prospect.io

To track mail open/reads, you need to add the tracking pixel to your campaigns or templates.&#x20;

Here are the steps needed for adding the tracking pixel:

1. go to your drip campaign or template
2. edit your campaign or template and switch to HTML (\</>)
3. paste in your email tracking pixel at the bottom\


{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=prospect.io&email={{prospect_email}}" width="1" height="1" class="fr-fic fr-dib">
```
{% endcode %}

**Notes:**

* Change datasetId to reflect yours
* Optionally, change the campaign value to reflect the email title or campaign name&#x20;
* you can add other template variables as parameters if you have them

### Track clicks and identify prospects on your site

To track email clicks, you need to modify your links to include these parameters&#x20;

example URL

{% code overflow="wrap" %}
```url
https://www.YOURDOMAINNAME.com?&firstName={{prospect_firstname}}&lastName={{prospect_lastname}}&email={{prospect_email}}&companyName={{prospect_company_name}}
```
{% endcode %}

For more details see these pages:

[https://support.prospect.io/hc/en-us/articles/115009231968-Create-Content-](https://support.prospect.io/hc/en-us/articles/115009231968-Create-Content-)

[https://support.prospect.io/hc/en-us/articles/115009483748-Template-Variables](https://support.prospect.io/hc/en-us/articles/115009483748-Template-Variables)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on March 7, 2019
