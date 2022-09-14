# Tracking Calendly Conversions on your site

If you are using Calendly to let people schedule meetings or appointments on your site, you can use LeadBoxer to identify these leads and see all their behaviour.

Here is what you need to do:

* Make sure you are using the Pro version of Calendly
* in your event settings, open the Confirmation page element and set it to redirect to a confirmation page and make sure to enable the "pass event details.." checkbox. This will add all the event details to the URL as parameters.
* On your site, create this confirmation page and make sure the LeadBoxer tracking pixel is installed
* You will need to add some javascript to grab the values from the URL and pass these to LeadBoxer:

```
<script>
var url_string = window.location.href
var url = new URL(url_string);
var invitee_full_name = url.searchParams.get("invitee_full_name");
var invitee_email = url.searchParams.get("invitee_email");
var answer_1 = url.searchParams.get("answer_1");
var answer_2 = url.searchParams.get("answer_2");
var answer_3 = url.searchParams.get("answer_3");
  
setTimeout(function(){ 
  if (invitee_email != null) {
	var map = new OTMap();    
	map.put("name", invitee_full_name);    
	map.put("email", invitee_email); <br>
	// add any additional fields like this
	map.put("companyName", answer_1); 
	map.put("title", answer_2);
	map.put("phoneNumber", answer_3);
	  
	OTLogService.sendEvent("meeting booked", map, false); 
	};
}, 1000);  


</script>
```

Thats it! \
You can now find these leads easily by setting a URL filter on your Confirmation page URL

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fc274364cedfd00165b4b97/file-fP060YlZn6.png)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on April 13, 2021
