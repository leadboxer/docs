# Google Tag Manager Data Layer Integration

If you would like to use data from your Data Layer and push it to LeadBoxer, you can do so by implementing the LeadBoxer onload function.

Here is an example snippet of javascript:

```
// setup the onload function
function ot_onload() {

  // find the tag manager container ID
  var tag = window.google_tag_manager
  var containerId;
  for (var key in tag) {
    if (key.startsWith("GTM")) {
      containerId = key;
      break;
    }
  }

  // next, set the variables you want to get from your data layer
  var primaryCategory = window.google_tag_manager[containerId].dataLayer.get("primaryCategory");
  var primaryCategoryList = window.google_tag_manager[containerId].dataLayer.get("primaryCategoryList");

  // put the values in a map     
  _otmap.put("primaryCategory", primaryCategory);
  _otmap.put("primaryCategoryList", primaryCategoryList);     
     
  // expose the variables for collection
  ot_log_state();
```

Above example allows you to get data from the Google Tag Manager Data Layer, and submit this to LeadBoxer,

**Important**:\
Now the only requirement is that this function needs to load **before** the default tracking javascript (aka LeadPixel)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on April 13, 2021
