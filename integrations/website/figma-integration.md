# Google Tag Manager (GTM)

### How to place the Lead Tracking Pixel in your website using Google Tag Manager (GTM)

Here are the basic steps needed to publish the Lead Pixel in your website and start converting anonymous traffic into leads.

Steps:

1. Login to your Google Tag Manager and access your container
2. To add the Lead Pixel, click on ‘add new tag’&#x20;
3.  Name your tag as LeadBoxer pixel or LeadPixel and select ‘custom HTML in the Tag Configuration section

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf1ec12c7d3a04dd5b8a2a/file-XMMheyuVPu.png" alt=""><figcaption></figcaption></figure>
4.  Cut & paste your Lead Pixel (grab this from your LeadBoxer email or welcome screen)

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf20bd2c7d3a04dd5b8a3d/file-7okdOvbb7b.png" alt=""><figcaption></figcaption></figure>
5.  Next you need to select or create your Trigger. We recommend to set it on all pageviews.

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf21c0042863158cc74cb9/file-lBUJmSoc1S.png" alt=""><figcaption></figcaption></figure>
6.  Save the trigger and the tag

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf22ca2c7d3a04dd5b8a57/file-PMMGKCZW8A.png" alt=""><figcaption></figcaption></figure>
7. Don't forget to Submit (publish) your changes - you’re done, you now have the basic Lead Pixel (javascript) working.

## Events

If you want to track on-page events using the Google Tag manager, you can follow these instructions .

1. Make sure the LeadBoxer pixel (script tag) is loaded on the initial pageview.
2.  You need to define the page title as a variable:&#x20;

    ```javascript
    function() {
      return document.title;
    }
    ```

    ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5f44f7ad042863444aa0cdeb/file-BLAXv0uQk4.png)
3.  Create and send a new event that triggers on every Custom Event.\


    ```javascript
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

```javascript
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
