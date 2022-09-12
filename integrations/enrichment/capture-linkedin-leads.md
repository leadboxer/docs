# Capture LinkedIn Leads

LeadBoxer can capture LinkedIn leads  from your visitor's . You do this by creating a LinkedIn login button and providing a reward. You reward visitor's who take an interest in your product or service in exchange for their LinkedIn's contact information.

To get started, you need to get the LinkedIn API framework setup at LinkedIn. The steps are described underneath.

### Step 1 Get a API key from linkedIn

Login at [https://developer.linkedin.com](https://developer.linkedin.com/)

Go the My Apps overview page, you can find this in the top navigation.

Create a New Application

Fill in the form:

### Create a New Application

* Select or create a new company
* Name: Download button
* Description: Download button for white-paper
* Application logo: select a logo
* Application Use: Sales (CRM), Marketing
* Website URL: the website where the button will be placed
* Business email: your email
* Business phone: your phone number
* Agree: tick the box
* Click Submit

Next screen is called  **Authentication**: you will need to change the Default Application: select r\_basicprofile and r\_emailaddress

Then go to the Javascript page and add the domains authorised to use this LinkedIn App

Note: We strongly encourage using HTTPS.

Now go back to the Authentication page and  **copy the Client ID (API Key).**

### Step 2: implementing the javascript snippet

Add the following into the \<head> section of the page.

```
<script type=”text/javascript” src=”https://platform.linkedin.com/in.js”>   
	api_key: < YOUR API KEY HERE >   
	authorize: true   
	onLoad: onLinkedInLoad
</script>
<script type=”text/javascript”>   
	function onLinkedInLoad() {      
		if (IN.User.isAuthorized()) { // do nothing as it is auth      
	} else {      
		window.location = “URL of page with download link“;      
		}   
	}
</script>
<script type="text/javascript">   // the functions needed for submitting to LeadBoxer  
function sendData(a){var b=new OTMap;b.put("firstName",a.values[0].firstName),b.put("lastName",a.values[0].lastName),b.put("email",a.values[0].emailAddress),void 0!=a.values[0].headline&&b.put("headline",a.values[0].headline),void 0!=a.values[0].summary&&b.put("summary",a.values[0].summary),void 0!=a.values[0].pictureUrl&&b.put("pictureUrl",a.values[0].pictureUrl),void 0!=a.values[0].publicProfileUrl&&b.put("publicProfileUrl",a.values[0].publicProfileUrl),void 0!=a.values[0].phoneNumbers&&b.put("phoneNumbers",a.values[0].phoneNumbers),void 0!=a.values[0].dateOfBirth&&b.put("dateOfBirth",a.values[0].dateOfBirth),void 0!=a.values[0].numConnections&&b.put("numConnections",a.values[0].numConnections),OTLogService.sendEvent("user download",b,!1)}function displayProfiles(a,b){member=a.values[0],sendData(a),setTimeout(function(){window.location=b},1e3)}function onLinkedInAuth(a){IN.User.authorize(function(){IN.API.Profile("me").fields(["id","firstName","lastName","industry","location:(name)","picture-url","headline","summary","num-connections","public-profile-url","distance","positions","email-address","educations","date-of-birth"]).result(function(b){displayProfiles(b,a)})})}function processRequest(a){onLinkedInAuth(a)}
</script>
```

And add a link to start the authentication, for example:

```
<a href="javascript:void(0);" onclick="processRequest('page2.html');" id="myLinkedInButton">download with linkedin</a>
```

See full working example here: [https://api.leadboxer.com/api/examples/linkedin/page1.html](https://api.leadboxer.com/api/examples/linkedin/page1.html)

### Step 3: Secure your content (optional)

Add the following into the **\<head>** section of the page, so that its only accessible when logged in with LinkedIn. If the user tries to access this page directly he or she will be redirected to the page with specified in 'window.location'.

```
<script type="text/javascript" src="https://platform.linkedin.com/in.js">
	api_key: < YOUR CLIENT ID /API KEY HERE >
	authorize: true
	onLoad: onLinkedInLoad
</script>
<script type="text/javascript">

   function onLinkedInLoad() {
      if (IN.User.isAuthorized()) {   // do nothing as it is auth
      } else {
      window.location = "page1.html";
      }
   }
</script>
```

[Example](https://api.leadboxer.com/api/examples/linkedin/page1.html)

[Login](https://product.leadboxer.com/go/) or [Start a free trial](https://www.leadboxer.com/?signup=true)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on June 23, 2018
