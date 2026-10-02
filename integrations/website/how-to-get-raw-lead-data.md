# How to get (raw) lead data

If you would like to retrieve all the data we have collected for a specific lead, you can do so using the [Retrieve Lead Details](https://developers.leadboxer.com/reference) call of the LeadBoxer API (`GET /v1/leads/{leadId}`).

This API call will return all the user data we currently have, including all the custom fields.

You can use this API call to generate dynamic or fluid content on your site, pass data to another service, or sync with another solution.

{% hint style="warning" %}
The API needs your LeadBoxer API key. Never put the API key in your website's JavaScript, where every visitor can read it. Call the API from your server (backend), and pass only the data you need to the browser.
{% endhint %}

### Speed and loading time

LeadBoxer data is captured and available in realtime and the lead details api returns data within a few milliseconds (eg 50).\
However, you should take into account that on the first initial pageview there could be a few seconds of overhead before we populate the lead or customer across our distributed datastore.&#x20;

Meaning that you should always build in some delay before you can access the lead details after the initial (first) event. &#x20;

**Workarounds**\
If many of your visitors click away or to another page quickly (eg within 2 seconds) you can try to load the lead details on the second pageview or process the data server-side with a few seconds delay.

### Example

In below example we read the visitor's LeadBoxer ID in the browser, send it to our own server, and the server gets the lead details and returns the city.

**Website (browser)**

```html
<!-- Load LeadBoxer tracking pixel
-- can be removed if pixel is already loaded using another method -->
<script src="//script.leadboxer.com/?dataset=yourDatasetId"></script>

<script type="text/javascript">
// first we add a 3s delay to make sure the lead is created before we can access the details
setTimeout(function () {
    var leadId = ot_uid(); // get current LeadBoxer lead ID

    // ask your own backend for the lead details
    fetch("/api/lead-city?leadId=" + encodeURIComponent(leadId))
        .then(function (response) { return response.json(); })
        .then(function (data) { console.log(data.city); });
}, 3000);
</script>
```

**Your server (Node.js example)**

```javascript
// GET /v1/leads/{leadId} returns all fields of one lead as JSON
async function getLeadCity(leadId) {
    const params = new URLSearchParams({
        email: "you@yourcompany.com",   // the email address you log in to LeadBoxer with
        site: "yourDatasetId"           // your dataset ID
    });
    const response = await fetch(`https://api.leadboxer.com/v1/leads/${encodeURIComponent(leadId)}?${params}`, {
        headers: { "x-api-key": process.env.LEADBOXER_API_KEY }
    });
    const lead = await response.json();
    return { city: lead.last_city };
}
```

See the [Developer Portal](https://developers.leadboxer.com/) for authentication, rate limits and all fields in the response.
