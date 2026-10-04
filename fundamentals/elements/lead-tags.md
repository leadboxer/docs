# Lead & Account Tags

### What are Lead Tags?

Lead Tags are tags or labels you can add to individual leads /users so you can easily see if they belong to a certain categorie.

### What are Account Tags?

Similar to Lead Tags, Account Tags allow you to tag leads or users, but account tags work a bit differently. If you set an Account Tag, LeadBoxer will apply this tag to all historical Leads from the same Account (organisation / company) AND all leads from this Account going forward.

### Why would I want to tag my Leads or Accounts?

Once you start tagging your leads, you can use the 'lead tag' filter to include or exclude leads from your filter pre-sets (views)/ segments.&#x20;

In plain English: (1) tag leads into general categories such as (existing) Customer, or Competitor, and then (2) filter your leads on these tags.

### Getting started with Lead Tags

Using tags is simple, and involves just 2 steps:

1.  **Manually tag a lead**\
    Using the LeadBoxer interface you can manually tag your leads in 2 different places: On the Lead details section or in the Leads & Accounts view. We have added 4 default tags: Competitor, Customer, Key account and Partner.  You can add additional tags yourself. There is a hard limit of 100 tags.<br>

    <figure><img src="../../.gitbook/assets/LeadBoxer_App (13).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../.gitbook/assets/LeadBoxer_App (2) (2) (1).png" alt=""><figcaption></figcaption></figure>
2.  **Set your Lead Tag filter**\
    Once you have added lead tags to your leads, you can use the filters to include or exclude them from/ to your Segments.<br>

    <figure><img src="../../.gitbook/assets/LeadBoxer_App (9) (1).png" alt=""><figcaption></figcaption></figure>

***

## Automatically tag leads

There are 2 options, using **Workflow Automation** or using the **LeadBoxer API**&#x20;

### 1. Workflow Automation

Use the **Add lead tag** action to automatically create or add a tag to lead based on a trigger. For example a specific page, or country.

<figure><img src="../../.gitbook/assets/Screenshot 2023-02-23 at 14.19.27.png" alt=""><figcaption></figcaption></figure>

See the Complete [Workflow Automation](workflow-automation.md) docs for more details.\
<br>

### 2. API

To tag leads automatically from your own systems, for example when a customer logs in to your site, use the [Update Lead Tags](https://developers.leadboxer.com/reference) call of the LeadBoxer API.

In other words: LeadBoxer monitors all traffic on your site and identifies companies and leads. By tagging everybody who logs in as a customer, you can filter your existing clients out of your lead views.

{% hint style="warning" %}
The API needs your LeadBoxer API key. Never put the API key in your website's JavaScript, where every visitor can read it. Call the API from your server (backend) instead.
{% endhint %}

**How it works**

1. In your website, read the visitor's LeadBoxer ID with `ot_uid()` (available once the LeadBoxer pixel has loaded) and send it to your own server, for example with the login request.
2. On your server, call the LeadBoxer API with your API key to set the tags.

**Website (browser)**

{% code overflow="wrap" %}
```javascript
<script defer src="//script.leadboxer.com/?dataset=yourDatasetId"></script>
<script type="text/javascript">
setTimeout(function () {   // small delay so the pixel has created the visitor and cookie
    var leadId = ot_uid(); // LeadBoxer ID of the current visitor

    // send the LeadBoxer ID to your own backend, which calls the LeadBoxer API
    fetch("/api/tag-customer", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ leadId: leadId })
    });
}, 3000);
</script>
```
{% endcode %}

**Your server (Node.js example)**

{% code overflow="wrap" %}
```javascript
// PUT /v1/management/lead-tags replaces all tags of the lead with the list you send.
// To add a tag and keep the existing ones, include the existing tags in the list.
async function tagCustomer(leadId) {
    await fetch("https://api.leadboxer.com/v1/management/lead-tags", {
        method: "PUT",
        headers: {
            "x-api-key": process.env.LEADBOXER_API_KEY,
            "Content-Type": "application/json"
        },
        body: JSON.stringify({
            datasetId: "yourDatasetId",
            leadId: leadId,
            leadTags: "customer"          // comma-separated, e.g. "customer,key account"
        })
    });
}
```
{% endcode %}

#### **Add, remove & overwrite tags**

The call sets the complete list of tags for the lead:

* **Add** a tag: send the existing tags plus the new one. You can read a lead's current tags with [Retrieve Lead Details](https://developers.leadboxer.com/reference) (`GET /v1/leads/{leadId}`).
* **Remove** a tag: send the existing tags without it.
* **Remove all** tags: send an empty `leadTags` value.

See the [Developer Portal](https://developers.leadboxer.com/) for authentication, rate limits and the full API reference.
