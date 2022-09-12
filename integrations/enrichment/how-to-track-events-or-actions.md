# How to track events or actions

### What are events?

LeadBoxer defines an event as a signal that is send to our service . An event can represent any type of activity, but usually is something that happens on a webpage that does not trigger a page load. For example a file download, or a single page website or app.

With the LeadBoxer Lead Pixel in place, you can track (log) any action or event in your web app or website.

The Lead Pixel contains functions and listeners that facilitate the insertion of events into LeadBoxer.

### Examples

**basic event**

```
<script src="//script.leadboxer.com/?dataset=YourDatasetId"></script> 
<script type="text/javascript">    
	OTLogService.sendEvent("basic event"); 
</script>
```

**basic event on pageload**

See the Pen [Track an event](https://codepen.io/LeadBoxer/pen/xxGLvda) by Wart Fransen ([@LeadBoxer](https://codepen.io/LeadBoxer)) on [CodePen](https://codepen.io/).

**Event with properties**&#x20;

LeadBoxer does not only support custom events, but also adding  [lead properties](https://docs.leadboxer.com/article/71-tagging-leads-with-properties)

```
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

```
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

### Events & Google Tag Manager

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

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on April 15, 2022
