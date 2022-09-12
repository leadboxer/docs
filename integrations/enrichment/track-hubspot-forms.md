# Track Hubspot forms

If you would like to track your Hubspot forms, here is how you can do it:

Requirements:

* Embedded Hubspot Form
* LeadBoxer account & pixel&#x20;

In this example we will only push the email value to LeadBoxer and associate this with the user-id from LeadBoxer

```
<script>
  hbspt.forms.create({
	region: "na1",
	portalId: "123",
	formId: "abc",
	onFormSubmit: function($form) {
		setTimeout(function(){   // we add a small delay 
			var email = $form.find('input[name="email"]').val();
			var userId = ot_uid();	        // define userID
		
			// Construct API call to add lead tag to the visitor
			var url = "https://log.leadboxer.com/?si=my-dataset-id&ti=Form-Submit&uid=" + userId + "&email=" + email;
  
			// send the data to the LeadBoxer API
			fetch(url,{mode: 'no-cors'});			
 		}, 500); // end of timeout function			
	}
});
</script>
```

Obviously you need to replace the various values with your own:

* form-field-name
* portalId
* formId
* my-dataset-id

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on November 25, 2021
