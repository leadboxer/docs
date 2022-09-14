# Advanced javascript/ pixel usage

This is a list of exposed javascript functions from the LeadBoxer tracking pixel.&#x20;

**ot\_uid()**\
Returns the LeadBoxer user ID that represents the user&#x20;

**ot\_sid()**\
Returns an internal ID that identifies the current session

#### **Adding properties on page load**

The LeadBoxer tracking script library, once loaded, will immediately check for a function called " **ot\_onload**". This is a hidden function that if defined, gets called. This function needs to be loaded before the script itself and needs to execute **ot\_log\_state**() - to actually append all data before the default request to our logging servers is made.&#x20;

The function needs to be in the html of the page, or if loaded externally, needs to be placed before the loading of Leadboxer script / pixel.&#x20;

A simple example looks like this:

```
<script type="text/javascript"> 
function ot_onload() {
  // define variables
  var CustomerId = "12345";
  var CustomerType = "Reseller";

  // add variables to map (_otmap)
  _otmap.put("Customer ID", CustomerId);  
  _otmap.put("Customer Type", CustomerType);

  ot_log_state();
}
</script>
```

Above example will add 2 additional properties to the lead or customer custom fields when the page loads.

**Reminder**: This function needs to be loaded before the default tracking script gets loaded.

### Static version of the javascript library

The Leadboxer tracking script or pixel is served form a high availability, low latency, geo-ip based custom build Content Delivery Network.&#x20;

It also is not a static javascript, meaning the code can change based on various use-cases/ scenario's.

However, in case you really want or need to load the javascript library from your own servers or location, you can accomplish this with these 2 steps:

1. Copy the contents of the hosted javascript to a local javascript file
2. Replace the variable ot\_t0 with a function that generates the current time in unixtime.\
   For example with the  **`Date.now()`** function&#x20;
3. Load this static javascript on your pages.
4. Test

Make sure you regularly rerun these steps, as we make changes to our hosted version the tracking javascript often.

**Important notice / disclaimer**

Some portions of the LeadBoxer javascript library are dynamically generated and provide customised code for advanced features like cross-device or cross-browser tracking, auto-form tracking and other functions. Meaning that the basic tracking features will work properly, but we do not guarantee that all advanced features work as designed when using a static version of our pixel.&#x20;

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on April 8, 2022
