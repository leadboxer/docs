# Google Tag Manager (GTM)

### How to place the Lead Tracking Pixel in your website using Google Tag Manager (GTM)

Here are the basic steps needed to publish the Lead Pixel in your website and start converting anonymous traffic into leads.

Steps:

1. Login to your Google Tag Manager and access your container
2. To add the Lead Pixel, click on ‘add new tag’&#x20;
3.  Name your tag as LeadBoxer pixel or LeadPixel and select ‘custom HTML in the Tag Configuration section

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf1ec12c7d3a04dd5b8a2a/file-XMMheyuVPu.png" alt=""><figcaption></figcaption></figure>
4.  Cut & paste your Tracking Pixel (grab this from your LeadBoxer welcome screen or find it on the dataset overview, right-click on the settings icon)

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf20bd2c7d3a04dd5b8a3d/file-7okdOvbb7b.png" alt=""><figcaption></figcaption></figure>
5.  Next you need to select or create your Trigger. We recommend to set it on all pageviews.

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf21c0042863158cc74cb9/file-lBUJmSoc1S.png" alt=""><figcaption></figcaption></figure>
6.  Save the trigger and the tag

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5bbf22ca2c7d3a04dd5b8a57/file-PMMGKCZW8A.png" alt=""><figcaption></figcaption></figure>
7. Don't forget to Submit (publish) your changes - you’re done, you now have the basic Lead Pixel (javascript) working.

## Events

If you want to track on-page events using the Google Tag manager, you can follow these instructions .

1. Make sure the LeadBoxer pixel (script tag) is loaded on the initial pageview.
2.  First you need to define a new variable to grab the page title (for some reason GTM does not provide this variable by default so we need to define it ourselves)\
    In your Google Tag Manager container, go to Variables > Javascript Variable and enter \


    ```javascript
    document.title
    ```



    ![](<../../.gitbook/assets/Google\_Tag\_Manager (3).png>)
3.  Create and send a new event that triggers on every Custom Event.\


    ```javascript
    <script type="text/javascript">    
    	var map = new OTMap();    
    	map.put("lc", {{Page URL}});    
    	OTLogService.sendEvent("{{Javascript - Page Title}}", map); 
    </script>
    ```



    ![](<../../.gitbook/assets/Google\_Tag\_Manager (4).png>)
4. Now connect this tag to any trigger you want: events, clicks, buttons, downloads, etc.
5. Don't forget to publish and you should be set.



### Complete Example: how to track a button click

1.  **In GTM, enable built-in Click Variables**\
    ****To be a able to trigger based on a click you need to enable these specific click variables. \
    Variables are little pieces of information that can be used both in Tags and Triggers. For example, **Click ID**. You can use it as a trigger condition (e.g. _fire the LeadBoxer Event code **when** the ID of the clicked link equals to “main-cta-link”_).

    <figure><img src="../../.gitbook/assets/Google_Tag_Manager (1).png" alt=""><figcaption></figcaption></figure>
2.  **In GTM tag assistant, Find the variable values to trigger on**\
    ****Go to preview mode and on your site, click on the button you want to track. Switch to the assistant mode and you should see the button click listed in your behaviour.\
    Select this click and find the right variable. (in our case the button text works, but you might want to use ID, class, URL or any of the above variables.) \
    Copy the variable value.\


    <figure><img src="../../.gitbook/assets/Tag_Assistant__Connected_.png" alt=""><figcaption></figcaption></figure>
3.  **in GTM, enable a link click trigger** \
    ****In order to enable link click tracking, we need to enable a thing called link click listener (a.k.a. link click auto-event listener). It’s a feature in GTM that listens to link clicks on a page. If it spots one, it will display that event in the GTM Preview and Debug (P\&D) mode, and we’ll be able to use it as a condition to fire tags. \
    In Google Tag Manager, go to Triggers > Trigger Configuration > New > Click - All elements. Set the trigger to only to fire on some Clicks and choose your variable from step 2.\


    <figure><img src="../../.gitbook/assets/Google_Tag_Manager (2).png" alt=""><figcaption></figcaption></figure>

    ****
4.  **Create a LeadBoxer Event tag to fire on this trigger**\
    Create a new tag, and add this javascript to send the custom event to LeadBoxer



    ```javascript
    <script type="text/javascript">    
    	var map = new OTMap();    
    	map.put("lc", {{Page URL}});    
    	OTLogService.sendEvent("Case study submit click", map); 
    </script>
    ```



    <figure><img src="../../.gitbook/assets/Google_Tag_Manager.png" alt=""><figcaption></figcaption></figure>


5. Don't forget to connect the tag from step 4 to the trigger from step 3 and also to publish the changes.





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
