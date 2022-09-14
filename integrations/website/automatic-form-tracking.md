# Automatic form tracking

Amazingly easy: Automatically send us all **\<Form>** data - when visitors fill in a form.

### Description

Automatic Form tracking can be easily enabled. This will allow us to auto-magically capture and track all (contact) details or form data submitted by ANY form.

Additionally, if you build the form-fields to match the [placeholder names](../../fundamentals/elements/import-and-export/leadboxer-user-interface-placeholder-names.md) we use, we will populate the LeadBoard in our LeadBoxer reporting interface with the data fields submitted by your visitors and leads. Alternatively, you can send you own custom data to LeadBoxer, which will then appear under Lead Properties on your Lead.

### Instructions

1. Log into your LeadBoxer account as an Admin
2.  Go to your datasets menu / overview \[[https://app.leadboxer.com/datasets\]](https://app.leadboxer.com/datasets]) and click the gear icon for the dataset you want to enable it for

    ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c8a2d590428633d2cf39550/dataset-gear-wheel.png)
3. Select settings: this should show a modal in where you can enable or disable the auto form tracking feature
4.  Enable the auto form tracking and save

    ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c8a2dc50428633d2cf39553/file-a7OY5t8n2M.png)
5. **Important**: Test your forms thoroughly, especially if you have complicated or custom-built forms.

#### Result

When you implement the code, your data will appear on your LeadBoard. Here is an example:

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5c88e2502c7d3a154460cbbf/file-A4jCxRnKIs.png)

### Implementation notes

* The field names that are automatically captured are taken from the 'name' of the form element
* The form submit button needs to be type='submit'

#### Optional improvements

If the field names that we capture are not properly defined, we recommend you alter them in your forms.

Adjust your form fields to match our pre-defined properties, for full integration in our app interface. These are the [placeholder names](../../fundamentals/elements/import-and-export/leadboxer-user-interface-placeholder-names.md) we use.

\<!DOCTYPE html>\
\<html lang= "en">\
\<head>\
\<meta charset= "utf-8">\
\<title>Example of Automatic Form Tracking - Example\</title>

\<!-- LEADBOXER START -->\
\<script type= "text/javascript"\
defer= "defer" src= "//script.leadboxer.com/?dataset=YourDataSetID\&form">\</script>\
\<!-- LEADBOXER END -->\
\</head>

\<body>\
\<form name= "myform" method= "post" action= "">\
\<label>email:\</label>\
\<input name= "email" type= "text" id= "email" value= "" />

\<label>\
company:\
\</label>\
\<input name= "companyName" type= "text" id= "companyName" />\
\<label>\
first name:\
\</label>\
\<input name= "firstName" type= "text" id= "firstName" />\
\<label>\
last name:\
\</label>\
\<input name= "lastName" type= "text" id= "lastName" />\
\<label>\
phone number:\
\</label>\
\<input name= "phoneNumber" type= "text" id= "phoneNumber" />\
\<input type= "submit" name= "submitForm" id= "submitForm" value= "Click to Submit" />

\</form>

\</body>

\</html>

[Example](http://api.leadboxer.com/api/examples/forms/index-script.html)

### Full control

If you prefer full control over the data that is being captured and submitted, you can try using manual form tracking. See the link below.

Still need help? [Contact Us](broken-reference)&#x20;

Last updated on March 14, 2019
