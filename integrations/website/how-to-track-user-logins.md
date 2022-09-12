# How to track user logins

### How to track and identify user/ clients/ customers when they log-in

In order to track user logins form your website, you can to collect client data from your system and pass this to their user profile:

### Submit data on load (preferred)

The LeadBoxer tracking script library, once loaded, will immediately check for a function called " ot\_onload". This is a hidden function that if defined, gets executed. **This function needs to be loaded before the script itself and needs to include ot\_log\_state()** - to actually append all data before the default request to our logging servers is made.&#x20;

A example looks like this:

```
<script type="text/javascript"> 
function ot_onload() {
  // define variables
  var customerId = "12345";
  var customerType = "Reseller";
  var customerEmail = "jack@website.com";

  // add variables to map (_otmap)
  _otmap.put("Customer ID", customerId);  
  _otmap.put("Customer Type", customerType);
  _otmap.put("email", customerEmail);

  ot_log_state();
}
</script>
```

Above example will add 3 additional properties to the lead or customer fields when the page loads.

Here is a list of recommend field-names: [https://docs.leadboxer.com/article/54-leadboxer-user-interface-placeholder-names](https://docs.leadboxer.com/article/54-leadboxer-user-interface-placeholder-names)

### Submit data on event

Alternatively, if you cant or do not want to submit details on page load, but want to trigger based on an event, you can use the Map function to submit data:

Paste the below snippet inside the page/file to add a custom tag. For example: use this to send us a signal when a user logs in to your system. We will add that information to visitor profiles. Send us login events; email addresses, usernames, LoginID, etc. You can also send us social media login events.

Make sure that: a. the default LeadBoxer javascript loads before the execution of below script b. the default LeadBoxer javascript should not contain the 'defer' tag. Alternatively you can wrap the script in a timeout or onPageLoad.&#x20;

A simple example looks like this:

```
<script type="text/javascript">

// define an empty variable called 'map' 
var map = new OTMap();

//define one or multiple properties to be added to the visitor profile, you need to replace the actual values with dynamic placeholders.
map.put("firstName", "Brad"); 
map.put("lastName", "Shaw"); 
map.put("email", "login@mysite.com"); 
map.put("companyName", "LeadBoxer"); 

//send (submit) the data to LeadBoxer 
OTLogService.sendEvent("Login added", map, false);

</script>
```

#### notes:

* Do not forget to replace the values of the lead or customer with dynamic data. eg \{{ firstName \}} (this depends on your language /platform)
* You can add as many properties as you like.
* You can change all the words that are inside quotes to suit your needs. For example you can dynamically generate the tag from your CMS
* To retrieve the data, you can use the LeadBoxer interface or our API

[Login](https://app.leadboxer.com/) or [Start a free trial](https://www.leadboxer.com/?signup=true)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on April 8, 2022
