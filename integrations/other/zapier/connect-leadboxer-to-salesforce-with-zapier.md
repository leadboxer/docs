# Connect Leadboxer to Salesforce with Zapier

This guide continues where [Getting started with LeadBoxer on Zapier](./) left off.

Select Salesforce as the tool you want to be triggered by Leadboxer.

![](https://lh5.googleusercontent.com/PuS7JEQ7XPt9Tiq\_A7Mh1jS6YRIZAhCBQILavuFzk9ilcaWCaJcOAI65pq700Bzi8ikjDyzYuJFn57Te38IkW-YV9cx9EZ\_1sBLBguwXpKHL5Qa1-hEqH-Ubo94VriCCFvgzSUvQ)

Choose ‘Find a lead’, this way you can make Zapier look through your existing Salesforce leads before adding a new one. It will update your lead if additional info is found and you can create a new lead if nothing is found in your Salesforce database.

![](https://lh6.googleusercontent.com/\_j6kQWMQ26ViLVnVxlTPWgY3uJdTt5d77GSiT4jWWAko2QxQ0cDzR\_vSU85dt0SJxC\_9GOObG14rU5zCuUnZJvxwnuGiEWNk2oUqgKt8pzHD8Q97xyVpx7FOmNhPZFQkfhM39B04)

Click ‘Connect a new account’, log in to your account and grant acces to Zapier. &#x20;

![](https://lh5.googleusercontent.com/oRIhQbJ992Idh3hkCIAfc--1zpwaBm5v\_aYe2aaOATouZzv4Vfmjdet\_PJiD-QThl\_RIyiDG\_\_gjPpkJk29ftk26byaOEoEyDgPG1EH4IS6gbDlTTLJw8MXe\_ye4hrFWGRnuncEH)

Edit the options to your preferences. Select ‘Field to search by’ to be company and the search value ‘Most likely company’ (out of the Leadboxer Variables). This way the tool will check whether the company is already in your Salesforce or not.

After this fill in all the variables the way you would like them to be presented in Salesforce.

Note that Last Name is required, but Leadboxer does not always detect a name right away. To solve errors related to this problem, add an extra value to the template that is always found i.e. Company name. In the field of ‘first name’ you can add multiple variables, so you can also attach the value of last name to this field.

You might want to add a filter before turning on your Zap, this way you can make sure only leads with sufficient information fill up your Salesforce pipeline. Where to add a filter is shown below.&#x20;

![](https://lh4.googleusercontent.com/0KCywBdDQe7B3Bn-NtMCP2K0xQqeCi746AbRhpIm4XLY05uYu7JtLic2tbqSJebZGeCwJvZBhEpEIabaWQnLRuX3opFMOZDF2bX82Ur-R2yq7bzS1DZl-Pts7RmN-KU5Y7rlXIEI)

For instance, you can enable that only leads with a known company name get processed by the system.&#x20;

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5758379fc697917dce6a6aac/file-uGtddfjwUt.png)

\
Simply test the Zap by clicking Create & Continue. Congratulations! You have a working

Zap, all you have to do now is turn it on!

Still need help? [Contact Us](broken-reference)

Last updated on June 8, 2016
