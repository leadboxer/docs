# Advanced Zapier usage

In this document we will give an example on how to use Zapier to talk to our API and perform complex or out of the box implementations

In this example case, a customer wanted to assign a lead in LeadBoxer based on the owner in their CRM (in this case Pipeline Deals)

This can be accomplished by setting up Zapier with these 5 steps (and you can make this more complex obviously if you need ;-)

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60253a19b3ebfb109b58154b/file-4KqbiCTsyP.png)

Here are the detailes for each step:

1\. Setup the LeadBoxer trigger and provide API key and select the correct dataset (website)

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60253aeab3ebfb109b581552/file-18ZLrIMMVe.png" alt=""><figcaption></figcaption></figure>

2\.  Add a filter (you can also add these later) to make sure the actions are only performed when a key event happens. In this case when a lead with a known email and a specific lead tag enters the system

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60253bf68502d1120e906784/file-0HmsknnnFn.png" alt=""><figcaption></figcaption></figure>

3\. Find the person / lead in the CRM based on the email (you can optionally create the person /deal/ etc but this is outside the scope of this tutorial)

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60253c6b24d2d21e45ed566f/file-s61VTG7eEp.png" alt=""><figcaption></figcaption></figure>

4\. Again you need a filter to match the owner ID of the person/lead/contact to the user ID in LeadBoxer. This also means you need to make a separate zap (duplicate) for each user/owner combination.

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60253e07661b720174a6c2c9/file-B54B8lEhn9.png" alt=""><figcaption></figcaption></figure>

5\. This is the most complex step, as it creates an API call to LeadBoxer and sets the 'assignee'. First you need to add the Webhooks by Zapier app and select the GET Action event

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60253e9c8502d1120e90679a/file-QWAa0lak9S.png" alt=""><figcaption></figcaption></figure>

Then you configure the webhook like this: the API URL is [https://kibana.leadboxer.com/api/management/assignLeads.jsp](https://kibana.leadboxer.com/api/management/assignLeads.jsp)

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60253f0b24d2d21e45ed5683/file-C5CDPZveUD.png)

Thats it

Now for every new lead (or existing lead with new activity)in leadboxer, where the email is known and the tag is set to team, we will search for that person in Pipedrive Deals, and assign the lead if the owner matches the filter.

You can of course also contact us and ask for our help
