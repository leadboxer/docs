# HubSpot

In this document you will find the steps needed to enable the HubSpot Integration

Description:\
The LeadBoxer HubSpot integration is a so-called two-way-sync between the 2 platforms:&#x20;

1. We collect contact details from HubSpot
2. Add these details to LeadBoxer&#x20;
3. We push enriched data back into HubSpot

#### What are the main benefits?&#x20;

* Create better performing (email) campaigns in HubSpot by using additional firmographic data when creating segments to deliver differentiating or customised messages&#x20;
* Let LeadBoxer fill in the gaps from HubSpot Business Insights. Local and smaller organisations are notably often not identified and enriched
* Improve linking to associated companies by enriching your contacts with their company domain name (even if they used a public email address like gmail.com)&#x20;
* Enable LeadBoxer to Identify known contacts to better filter, or segment out various groups within your audience. Eg: Identify new business vs upsell opportunities&#x20;

How does the integration work:

We grab the HubSpot cookie ID from your website visitors, and use this to lookup the contacts in HubSpot. For existing contacts (ie not anonymous web visitors), we collect the contact details (name, email, company, etc) and add this to the Leads in LeadBoxer for use in our Firmographic enrichment process. Any enriched field can then be pushed back to update these Hubspot contacts.&#x20;

Additionally, you can define any fields that you want to sync back and forth between the LeadBoxer and HubSpot platforms. To get started, let us know your fields and we will setup  mapping. By default we enable First Name, Last Name, Email and Company Name. Recommended fields are Company Size, Industry and Domain, however we can add as many fields as you like.

#### How to enable:

1. Log into your LeadBoxer account as admin and go to the HubSpot Integrations page.
2.  Click on the Enable Integration button and select the HubSpot account you want to connect to.

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/61449d902b380503dfdf239a/file-58peNdPpOD.png" alt=""><figcaption></figcaption></figure>
3.  authorise with your HubSpot Admin credentials

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/61449da72b380503dfdf239b/file-yKzY3I8HXE.png" alt=""><figcaption></figcaption></figure>
4.  Enable the integration, select the dataset you want to connect to and click save.

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/61449d8000c03d6720758130/file-hfsvzY81Ay.png" alt=""><figcaption></figcaption></figure>
5. Optionally, if you have multiple teams configured in HubSpot, and you want us to only sync contacts from a specific team, you can enter the team Id's here.

Please let us know if you have any questions or remarks.



## Track HubSpot forms

If you would like to track your HubSpot forms, here is how you can do it:

Requirements:

* Embedded Hubspot Form
* LeadBoxer account & pixel&#x20;

In this example we will only push the email value to LeadBoxer and associate this with the user-id from LeadBoxer

```javascript
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
