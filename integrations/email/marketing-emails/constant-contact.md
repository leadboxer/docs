# Constant Contact

Constant contact offers 2 products to send email:&#x20;

1. Email & Digital Marketing
2. Lead Gen & CRM

### Email & Digital Marketing

1. Tracking Email open events

For Email & Digital Marketing, they currently do not offer the option to add edit HTML (which is needed to add a tracking pixel).&#x20;

They do offer a Zapier integration, so you will be able to send email open events to LeadBoxer using the [Zapier webhook](../../other/how-to-get-started-with-leadboxer-on-zapier/zapier-webhook.md) method.&#x20;

2. Tracking email link clicks

For tracking email link clicks and identifying the recipient-visitor on your website, you can use the generic method by appending variables to the links in your emails (example):

{% code overflow="wrap" %}
```
https://yourdomain.com/?firstName=[[firstName]]&lastName=[[lastName]]&email=[[emailAddress]]&companyName=[[account.organizationName]]
```
{% endcode %}

Official Documentation can be found here

[Insert dynamic links in an email](https://knowledgebase.constantcontact.com/email-digital-marketing/articles/KnowledgeBase/38461-Insert-Dynamic-Links-in-an-Email?lang=en_US)

### Lead Gen & CRM

Tracking Pixel example



{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=CAMPAIGNNAME&email={$emailAddress}"/>
```
{% endcode %}

If you want to pass additional details you can do so:

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId=YOUR DATASET ID&campaign=CAMPAIGNNAME&firstName={$firstName}&lastName={$lastName}&email={$emailAddress}&companyName={$companyName}"/>
```
{% endcode %}

That should take care of tracking email opens.

For tracking email clicks and identifying your readers on your site you should similarly append these variables to the links in your emails (example):

{% code overflow="wrap" %}
```url
https://yourdomain.com/?firstName={$firstName}&lastName={$lastName}&email={$emailAddress}&companyName={$companyName}
```
{% endcode %}

You can add custom properties as well if they are stored in your database. See details here:

[official docs](https://knowledgebase.constantcontact.com/lead-gen-crm/articles/KnowledgeBase/50529-Available-Lead-Gen-CRM-Merge-Variables?lang=en_US)
