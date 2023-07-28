# Gravity Form Tracking

If you want to track your forms and use the Gravity Forms Wordpress plugin, you can use our official [LeadBoxer for Gravity Forms add-on ](https://wordpress.org/plugins/leadboxer-gravityforms/)

### How to use Gravity Form add-on for LeadBoxer

Here are the steps:

1.  Install and activate the Wordpress plugin like you would normally do: either searching for it on the plugins page or by downloading/uploading.

    1.  If you do not have gravity Forms installed you will get a error and warning.

        <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/62d16e8203382e4311cf4e01/file-scFSAbRhzz.png" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/62d16e33eabe9a7235b3e21e/file-YkXZDhhjhi.png" alt=""><figcaption></figcaption></figure>
2.  Once installed and activated, you need to configure / add your dataset ID in the global gravity Forms Plugin settings

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/62d16f95eabe9a7235b3e22a/file-KsqmRg93U4.png" alt=""><figcaption></figcaption></figure>
3.  Next, you need to map your form fields to the correct default LeadBoxer field names for each form.

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/62d17032d242501d78c64cf0/file-iIdJqMJe5U.png" alt=""><figcaption></figcaption></figure>
4.  If you have form fields that cannot be mapped to a default LeadBoxer field, you can add manual mappings. These form fields and values will be shown under Lead Properties. you can add up to 20 custom fields.

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/62d170fac74a080359c8a1fd/file-t87PUuQ7FP.png" alt=""><figcaption></figcaption></figure>

### Thats it.



**Manual setup (legacy)**

If you do not want or can use our Add-on you can try one of these manual / legacy integrations:

will need to manually add some javascript to your pages to make this happen.

There are multiple ways to accomplish this goal. Lets show you 2 options.

**Submit form data when the Confirmation message loads (recommended)**

Simply go to the confirmation settings for your form, switch to 'text' view and append a snippet of javascript like this:

```
<script type="text/javascript">
  var map = new OTMap();

  var emailTextbox = '{Email:4}'
  var nameTextbox = '{Name:2}'
  var phoneTextbox = ' {Phone:5}'
  var messageTextbox = '{Message:7}'

  map.put("email", emailTextbox);
  map.put("name", nameTextbox);
  map.put("phone", phoneTextbox);
  map.put("message", messageTextbox);

  OTLogService.sendEvent("Contact form submitted", map);
</script>
```

You will need to&#x20;

* replace the variables like {Email:4} with the form specific values.&#x20;
* Add all the form fields you want to track

You can use the form field dropdown to insert them. ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/6284cd3ac01fce37d9b1442d/file-IGwGOfG3gp.png)

### Option 2, Listen on form submit

You will need to go through these 2 steps:

1. Add a function to execute the tracking code when someone clicks on the submit button and
2. Grab the values of all your form elements and send them to our endpoint.

#### Step 1, trigger the tracking code on submit&#x20;

First you will need to find the ID of the submit button, eg 'gform\_submit\_button\_1' and use this in a javascript to execute the form tracking function when someone clicks the submit button in your form.

```
<script type="text/javascript">
jQuery('#gform_submit_button_1').on('click', function(){
	sendTextForm();
	console.log("click");
	});
</script>
```

#### Step 2, collect the form data and transfer

in step 1, we are executing a function called 'sendTextForm' once the submit button is clicked.&#x20;

In this step we create this function in where we are going to grab the values of the form fields.&#x20;

**Note:**\
As you may know, Gravity forms has dynamically generated form ID's so that makes it a little harder to grab the right fields, but by using your browser dev tools/ inspector you should be able to figure this out.

Here is an example of the actual function:

```javascript
<script type="text/javascript">
function sendTextForm() {
	
	var map = new OTMap();
		
	var emailTextbox = document.getElementById("input_4_3").value;
	var companyTextbox = document.getElementById("input_4_2").value;
	var nameTextbox = document.getElementById("input_4_1").value;
	var titleTextbox = document.getElementById("input_4_4").value;
	var phoneNoTextbox = document.getElementById("input_4_5").value;
	
	// add the form field to the map
	map.put("email", emailTextbox);
	map.put("company", companyTextbox);
	map.put("name", nameTextbox);
	map.put("title", titleTextbox);
	map.put("phoneNumber", phoneNoTextbox);
		
	OTLogService.sendEvent("Contact demo form submitted", map);
	console.log("submit");
}
</script>
```

Thats it, place both pieces of javascript on your form page (and make sure the tracking pixel is loaded as well) and you should see your form submissions appear in LeadBoxer.

Feel free to contact us if you would like us to help.
