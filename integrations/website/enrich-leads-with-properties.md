# Enrich leads with properties

Adding properties to a lead is very straightforward.&#x20;

Simply add the property name and value you wish to add by using LeadBoxer's map javascript feature.

1. Create a property container (map)
2. add/define the properties&#x20;
3. send/submit the data to be attached to the lead&#x20;

**Basic Example:**

```
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

| <p><strong>var map = newOTMap();</strong><br></p> | <p>define an empty variable called 'map'<br></p>                            |
| ------------------------------------------------- | --------------------------------------------------------------------------- |
| **map.put**                                       | <p>insert data into an object (map) as a property name/ value pair.<br></p> |
| **map.get**                                       | <p>read a previous value set <br></p>                                       |
| **map.clear**                                     | used to clear all the data in a                                             |
| **map.remove**                                    | use to remove specific property from a map                                  |

Once your map has been defined, you can send it to us with a simple javascript function:

```
OTLogService.sendEvent("your event title", map); :
```

This function will send (submit) the data to our log servers.

**Examples**

Add multiple properties to a lead

```
<script type="text/javascript" src="https://script.leadboxer.com/?dataset=YourDatasetId"></script> 

<script type="text/javascript">    
	var map = new OTMap();    
	map.put("firstName", "John");    
	map.put("lastName", "Doe");   
	OTLogService.sendEvent("my custom event", map); 
</script>
```

Add a tag for email campaign

```
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

Still need help? [Contact Us](broken-reference)

Last updated on April 15, 2022
