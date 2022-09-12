# How to get (raw) lead data

If you would like to retrieve all the data we have collected for a specific lead, you can do so using the LeadDetail API call.

This API call will return all the user data we currently have, including all the custom fields.

You can use this API call in your site to generate dynamic or fluid content, pass data to another service or use this server-side to sync with another solution.

### Speed and loading time

LeadBoxer data is captured and available in realtime and the lead details api returns data within a few milliseconds (eg 50).\
However, you should take into account that on the first initial pageview there could be a few seconds of overhead before we populate the lead or customer across our distributed datastore.&#x20;

Meaning that you should always build in some delay before you can access the lead details after the initial (first) event. &#x20;

**Workarounds**\
If many of your visitors click away or to another page quickly (eg within 2 seconds) you can try to load the lead details on the second pageview or process the data server-side with a few seconds delay.

### Example

In below example we will load the city for the current browser and show this in the console

```
<!-- Load LeadBoxer tracking pixel 
-- can be removed if pixel is already loaded using another method -->    
<script src="//script.leadboxer.com/?dataset=ee84d5e06e8811e79a2675ee660df0b1"></script> 

<!-- Load jQuery 
-- can be removed if lib is already loaded using another method -->
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>  



<script type="text/javascript">

// first we add a 3s delay to make sure the lead is created before we can access the details
setTimeout(function(){   
  //   Variables for lead details API
  var leadId = ot_uid();                         // get current LeadBoxer userID
  var site = "ee84d5e06e8811e79a2675ee660df0b1"; // define your datasetID
  
  // Construct url for lead_details API
  var url = "https://kibana.leadboxer.com/api/views/lead_detail?email=&leadId=" + leadId + "&site=" + site;


  // In this example, we will get the lead details and output the last_city using jQuery to parse the json data
  $( document ).ready(function() {

    jQuery.ajax({
    url: url,
    dataType: 'jsonp',
    success: function(data) {
      last_city = data.resultsList[0].last_city;
      console.log(last_city);
	  }
	});
  });

}, 3000); // end of timeout function	

</script>
```

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on September 4, 2020
