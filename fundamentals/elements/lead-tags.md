# Lead Tags

### What are Lead Tags?

Lead Tags are tags or labels you can add to your leads /users in order to group them into categories.

### Why would I want to tag my leads?

Once you start tagging your leads, you can use the lead tag filter to include or exclude leads from your filter pre-sets (views)/ segmentS.&#x20;

In plain english: you tag leads into general categories such as (existing) Customer, or Competitor, and then filter your leads on these tags.

### Getting started with Lead Tags

Using tags is simple, and involves just 2 steps:

1.  **Manually Tag a lead**\
    Using the LeadBoxer interface you can manually tag your leads on 2 different places: On the Lead details section or in the Leads & Accounts view. We have added 4 default tags: Competitor, Customer, Key account and Partner.  Obviously you can add other tags yourself. There is a hard limit of 100 tags.\


    <figure><img src="../../.gitbook/assets/LeadBoxer_App (13).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../.gitbook/assets/LeadBoxer_App (2) (2).png" alt=""><figcaption></figcaption></figure>
2.  **Set your Lead Tag filter**\
    Once you have added lead tags to your leads, you can use the filters to include or exclude them from/ to your Segments.\


    <figure><img src="../../.gitbook/assets/LeadBoxer_App (9) (1).png" alt=""><figcaption></figcaption></figure>

***

## Automatically tag leads

There are 2 options, using **Workflow Automation** or using **javascript**&#x20;

### 1. Workflow Automation

Use the **Add lead tag** Action to automatically create or add a tag to lead based on a trigger. For example a specific page, or country.

<figure><img src="../../.gitbook/assets/Screenshot 2023-02-23 at 14.19.27.png" alt=""><figcaption></figcaption></figure>

See the Complete [Workflow Automation](workflow-automation.md) docs for more details.\
\


### 2. Javascript

In order to automatically tag leads or visitors, use the Update Lead Tag API call. Use this API call to set new Lead Tags from your website, for example when customers login.

In other words - LeadBoxer monitors all traffic on your site - identifies companies and leads. By using this functionality - you can automate the process of filtering out your existing client database - by effectively excluding (tagging) everybody who logs in.

**Javascript Example**\


In below example we take the LeadBoxer user ID from the LeadBoxer cookie and use it to send a signal to our servers with the Lead Tag: customer

{% code overflow="wrap" %}
```javascript
<script defer src="//script.leadboxer.com/?dataset=yourDatasetId"></script>
<script type="text/javascript">

setTimeout(function(){   // we add a small delay to make sure the visitor and cookie are created before we use it
		
   var leadTag = "customer"		// define the lead tag
   var userId = ot_uid();	        // define userID
		
   // Construct API call to add lead tag to the visitor
   var url = "https://kibana.leadboxer.com/api/management/update_lead_tags?action=add&userId=" + userId + "&leadTags=" + leadTag;
  
   // send the data to the LeadBoxer API
   fetch(url,{mode: 'no-cors'});			
				
   // optional logging		
   console.log("Added customer tag to userId: " + userId);
	
 }, 3000); // end of timeout function			
</script>
```
{% endcode %}

#### **Add, remove & overwrite tags**

You can use these parameters to add or remove specific tags:  _**\&action=add**_ or _**\&action=remove**_

**NOTE:**\
If you do not provide one of these parameters, then the request will overwrite all existing tags that are already present.
