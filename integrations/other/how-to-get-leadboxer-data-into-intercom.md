# How to get LeadBoxer data into Intercom

### LeadBoxer and Intercom

If you are using Intercom, and you want to have some of the data from a LeadBoxer profile added to your intercom leads or users, you can do this by using some javascript to send any LeadBoxer property to Intercom as 'custom data'.

For example, you might want to add the Company name or a tag that that you have set using LeadBoxer, or even a the link to the full LeadBoxer profile, aka the LeadCard.

### How to do it?

Assuming you have both the LeadBoxer and Intercom javascript /pixel installed:

1. Read the LeadBoxer lead ID from the cookie with `ot_uid()`. (The cookie is set on the first view, so this will fail on the first pageview.)
2. Build the link to the LeadCard from the lead ID and your dataset ID. This needs no API call.
3. Send the data to Intercom using their [update](https://developers.intercom.com/installing-intercom/web/methods#intercomupdate) function.

```html
<!-- Load Intercom -->
<script>
  var APP_ID = "YOUR APP ID";    // <-- make sure you update this
  window.intercomSettings = {
    app_id: APP_ID
  };
</script>
<script>(function(){var w=window;var ic=w.Intercom;if(typeof ic==="function"){ic('reattach_activator');ic('update',intercomSettings);}else{var d=document;var i=function(){i.c(arguments)};i.q=[];i.c=function(args){i.q.push(args)};w.Intercom=i;function l(){var s=d.createElement('script');s.type='text/javascript';s.async=true;s.src='https://widget.intercom.io/widget/APP_ID';var x=d.getElementsByTagName('script')[0];x.parentNode.insertBefore(s,x);}if(w.attachEvent){w.attachEvent('onload',l);}else{w.addEventListener('load',l,false);}}})()</script>

<!-- Load LeadBoxer -->
<script src="//script.leadboxer.com/?dataset=yourDatasetId"></script>

<script type="text/javascript">
setTimeout(function () {
  var leadId = ot_uid();         // LeadBoxer lead ID of the current visitor
  var site = "yourDatasetId";    // your dataset ID

  // Link to the LeadCard in LeadBoxer
  var leadcard_url = "https://app.leadboxer.com?q=" + leadId + "&site=" + site;

  // Send data to Intercom
  Intercom('update', {"leadcard": leadcard_url});
}, 3000);
</script>
```

### Other LeadBoxer properties

To send other LeadBoxer data to Intercom, such as the company name or lead tags, get it from the LeadBoxer API with [Retrieve Lead Details](https://developers.leadboxer.com/reference) (`GET /v1/leads/{leadId}`). The API needs your API key, so make this call from your server and never from your website's JavaScript. See [How to get (raw) lead data](../website/how-to-get-raw-lead-data.md) for a complete example.

Still need help? [Contact us](mailto:hello@leadboxer.com)

Last updated on August 14, 2020
