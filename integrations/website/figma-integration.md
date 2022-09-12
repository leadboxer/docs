# Google Tag Manager (GTM)

##

##

## Events & Google Tag Manager

If you are using the Google Tag manager, See instructions below.

1. Obviously the LeadBoxer pixel (script tag) needs to be loaded on the initial pageview.
2.  You need to define the page title as a variable: \


    ```
    function() {
      return document.title;
    }
    ```

    ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5f44f7ad042863444aa0cdeb/file-BLAXv0uQk4.png)
3.  Create and send a new event that triggers on every Custom Event.\


    ```
    <script type="text/javascript">    
    	var map = new OTMap();    
    	map.put("lc", {{Page URL}});    
    	OTLogService.sendEvent("{{GA PageTitle}}", map); 
    </script>
    ```

    ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5f44f5d9042863444aa0cdd7/file-2LVgTG8MTi.png)
4. Don't forget to publish and you should be set.

## Google Tag Manager Data Layer Integration

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
