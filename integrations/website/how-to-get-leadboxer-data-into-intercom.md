# How to get LeadBoxer data into Intercom

### LeadBoxer and Intercom

If you are using Intercom, and you want to have some of the data from a LeadBoxer profile added to your intercom leads or users, you can do this by using some javascript to send any LeadBoxer property to Intercom as 'custom data'.

For example, you might want to add the Company name or a tag that that you have set using LeadBoxer, or even a the link to the full LeadBoxer profile, aka the LeadCard.

### How to do it?

Assuming you have both the LeadBoxer and Intercom javascript /pixel installed. You need to do the following:

1. Read the LeadBoxer user ID from the cookie. (The cookie is set on the first view, so this will fail on the first pageview)
2. Construct an API call to get the data for the current user
3. Get the actual data from leadBoxer (To get to the json data we use jQuery, but you can also use other libraries or natie JS)
4. Send the data to Intercom using their [update](https://developers.intercom.com/v2.0/docs/intercom-javascript#section-intercomupdate) function

```
<!-- Load jQuery -->
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>

<!-- Load Intercom -->
<script>
  var APP_ID = "YOUR APP ID";    // <-- make sure you update this
  window.intercomSettings = {
    app_id: APP_ID
  };
</script>
<script>(function(){var w=window;var ic=w.Intercom;if(typeof ic==="function"){ic('reattach_activator');ic('update',intercomSettings);}else{var d=document;var i=function(){i.c(arguments)};i.q=[];i.c=function(args){i.q.push(args)};w.Intercom=i;function l(){var s=d.createElement('script');s.type='text/javascript';s.async=true;s.src='https://widget.intercom.io/widget/APP_ID';var x=d.getElementsByTagName('script')[0];x.parentNode.insertBefore(s,x);}if(w.attachEvent){w.attachEvent('onload',l);}else{w.addEventListener('load',l,false);}}})()</script>      

<!-- Load LeadBoxer -->    
<script src="//script.leadboxer.com/?dataset=ee84d5e06e8811e79a2675ee660df0b1"></script> 


<script type="text/javascript">

  //   Variables for lead_details
  var userId = ot_uid();                         // define userID
  var site = "ee84d5e06e8811e79a2675ee660df0b1"; // your datasetID
  
  // Contruct url for lead_details
  var url = "https://kibana.leadboxer.com/api/views/lead_detail?email=&leadId=" + leadId + "&site=" + site;

  $( document ).ready(function() {

    // In this example, we will get the lead details and output the leadcard URL
    jQuery.ajax({
    
    url: url,
    dataType: 'jsonp',
    success: function(data) {
      leadcard_url = data.resultsList[0].leadcard_url;
      console.log(leadcard_url);
      
      // Send data to Intercom
      Intercom('update', {"leadcard": leadcard_url});
      }
  });
});
</script>
```

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on August 14, 2020
