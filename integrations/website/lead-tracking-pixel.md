# Lead Tracking Pixel

**Definition Lead Pixel**: a code snippet you get from LeadBoxer and place in one or more pages in your website. Any visitor to that page activates the pixel and is then captured as a potential lead. The Lead Pixel functions to a) identify the company behind the visit and b) record all future visits by that lead.

**How it works**: Drop the Lead Pixel (JavaScript code snippet) in your site. Once in place, the pixel generates a list of leads - names of companies interested in your products and services, based on your website traffic.

**Where to put it**: Track incoming leads across your whole website. You can also put the pixel into individual landing pages. Examples would be a contact form or newsletter sign-up form. You can  integrate the pixel directly, use  our [WordPress plugin](wordpress-plug-in/), or get an API license. \
If integrated directly, the **Lead Pixel needs to be placed in the source code** of all the webpage(s) that you wish to track. The best place is the footer - this will place the tracking code in the whole site, and takes less than 5 minutes.

**What you can accomplish with a Lead Pixel**:\
1\. Generate a list of qualified leads - companies interested in your product/service - based on their interest in your site.\
2\. Prioritise leads based on leadscore - automatically sort through all incoming leads using big data algorithms to score based on quality\
3\. Track all activity on your site by (potential) leads - during sales cycles and beyond

[Get your Lead Pixel](https://www.leadboxer.com/?signup=true)

#### Introduction

By installing the LeadBoxer Tracking Pixel on your website(s), we will automatically start to collect data and provide more information about your website visitors.

The LeadBoxer Tracking Pixel is a small snippet of javascript that will track all **users** (visitors), **sessions** (visits) and **events** (pageviews) for all the pages you install it on.

Once the Pixel is in place, we immediately start tracking and identifying your leads and customers. &#x20;

#### Installation

If you havent done so already, the first step is to [Start a trial](https://www.leadboxer.com/start/) at leadboxer.com - you will then receive the Pixel (code snippet) from us.

You can use any of the following plugins / tutorials to get started:\


* [Wordpress](wordpress-plug-in/)
* Drupal
* [Google Tag Manger](figma-integration.md)
* [Unbounce](track-unbounce-landing-pages.md)

**Other / Manual installation**

If you do not use any of above solutions, simply paste your Lead Pixel into the source code of your website just before the end \</body> tag. The best place is the footer or template - this will place the tracking code in the whole site, and usually takes less than 5 minutes.

#### Where to find your tracking Pixel or dataset ID

The tracking pixel and/or dataset ID can be found here:

#### Adding extra sites (datasets)

You can add extra datasets to your LeadBoxer account.

This can be accomplished in the datasets overview:

After adding your dataset(s) you can also give permission to team members to access the data.

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c471dee2c7d3a66e32d7c70/file-Anv46pNpYQ.png" alt=""><figcaption></figcaption></figure>

Note: You need to have admin rights to be able to see/do this.

Adding properties to a lead is very straightforward.&#x20;

Simply add the property name and value you wish to add by using LeadBoxer's map javascript feature.

1. Create a property container (map)
2. add/define the properties&#x20;
3. send/submit the data to be attached to the lead&#x20;

**Basic Example:**

```javascript
<script>

// define an empty variable called 'map'
var map = new OTMap();    

//define a property + value to be send to tag the lead
map.put("gender","male");

//send (submit) the data to LeadBoxer
OTLogService.sendEvent("gender logged", map);

</script>
```

#### Usage

These are de functions you can use for adding properties using a map

| **var map = newOTMap();** | define an empty variable called 'map'                            |
| ------------------------- | ---------------------------------------------------------------- |
| **map.put**               | insert data into an object (map) as a property name/ value pair. |
| **map.get**               | <p>read a previous value set <br></p>                            |
| **map.clear**             | used to clear all the data in a                                  |
| **map.remove**            | use to remove specific property from a map                       |

Once your map has been defined, you can send it to us with a simple javascript function:

```javascript
OTLogService.sendEvent("your event title", map);
```

This function will send (submit) the data to our log servers.

**Examples**

Add multiple properties to a lead

```javascript
<script type="text/javascript" src="https://script.leadboxer.com/?dataset=YourDatasetId"></script> 

<script type="text/javascript">    
	javavar map = new OTMap();    
	map.put("firstName", "John");    
	map.put("lastName", "Doe");   
	OTLogService.sendEvent("my custom event", map); 
</script>
```

Add a tag for email campaign

```javascript
<script type="text/javascript" src="https://script.leadboxer.com/?dataset=YourDatasetId"></script> 
<script type="text/javascript"> 
	var map = new OTMap();    
	map.put("utm_campaign", "event registration"); 
	map.put("utm_source", "Mailchimp"); 
	map.put("umm_medium", "email"); 
	OTLogService.sendEvent("my custom event", map);
</script>
```

#### Working example

A working example can be found here:  [http://api.leadboxer.com/api/examples/log/index.html](http://api.leadboxer.com/api/examples/log/index.html)

## Advanced

This is a list of exposed javascript functions from the LeadBoxer tracking pixel.&#x20;

**ot\_uid()**\
Returns the LeadBoxer user ID that represents the user&#x20;

**ot\_sid()**\
Returns an internal ID that identifies the current session

#### **Adding properties on page load**

The LeadBoxer tracking script library, once loaded, will immediately check for a function called " **ot\_onload**". This is a hidden function that if defined, gets called. This function needs to be loaded before the script itself and needs to execute **ot\_log\_state**() - to actually append all data before the default request to our logging servers is made.&#x20;

The function needs to be in the html of the page, or if loaded externally, needs to be placed before the loading of Leadboxer script / pixel.&#x20;

A simple example looks like this:

```javascript
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





### What are events?

LeadBoxer defines an event as a signal that is send to our service . An event can represent any type of activity, but usually is something that happens on a webpage that does not trigger a page load. For example a file download, or a single page website or app.

With the LeadBoxer Lead Pixel in place, you can track (log) any action or event in your web app or website.

The Lead Pixel contains functions and listeners that facilitate the insertion of events into LeadBoxer.

### Examples

**basic event**

```javascript
<script src="//script.leadboxer.com/?dataset=YourDatasetId"></script> 
<script type="text/javascript">    
	OTLogService.sendEvent("basic event"); java
</script>
```

**basic event on pageload**

See the Pen [Track an event](https://codepen.io/LeadBoxer/pen/xxGLvda) by Wart Fransen ([@LeadBoxer](https://codepen.io/LeadBoxer)) on [CodePen](https://codepen.io/).

**Event with properties**&#x20;

LeadBoxer does not only support custom events, but also [adding lead properties](lead-tracking-pixel.md#adding-properties-on-page-load)

```javascript
<script src="//script.leadboxer.com/?dataset=YourDatasetId"></script> 
<script type="text/javascript">    
	var map = new OTMap();    
	map.put("firstName", "John");    
	map.put("lastName", "Doe");    
	OTLogService.sendEvent("my custom event", map); 
</script>
```

**Example: Track a PDF download link**

To measure a click on a link that downloads a file, you can add a small piece of javascript to track this download:

```javascript
<!-- Load the LeadBoxer javascript before you define the custom variable -->
<script src="//script.leadboxer.com/?dataset=YourDatasetId"></script> 
<script type="text/javascript">

function downloadlink(file) {
	var map = new OTMap();    
	map.put("PDF", file);
	OTLogService.sendEvent("Download", map, false); 

	// add 1 second delay so the event registers before downloading
	setTimeout(function() {
		window.location=file;
	},1000); 
}; 
</script>

<p><a href="#" onclick="downloadlink('mypdf.pdf');">Download PDF</a></p>
<p><input onclick="downloadlink('mypdf.pdf');" type="button" value="Download PDF" /></p>
```

#### Working example

A working example can be found here:  [http://api.leadboxer.com/api/examples/log/index.html](http://api.leadboxer.com/api/examples/log/index.html)

###
