# Marketo

In this document you will find the steps needed in order to enable the Marketo Integration

**Note:**\
**Marketo is a Premium Integration, meaning you need a Premium subscription to use this integration. Please contact sales if you would like to learn more.**

Description:

The LeadBoxer Marketo integration is a so-called two-way-sync between the 2 platforms:

We (1) collect contact details from Marketo, (2) add these to LeadBoxer and (3) push enriched data back into Marketo.

In detail, we grab the Munchkin Marketo cookie ID, and use this to lookup the contacts in Marketo. For known contacts only (ie not anonymous web visitors), we collect the contact details and add these to the leads in LeadBoxer, triggering our firmographic enrichment process. The enriched fields can then be pushed back to update the Marketo contacts.

1. LeadBoxer enables the automatic Munchkin Marketo cookie ID capture
2. You define the fields that you want to sync back and forth between the LeadBoxer and Marketo and we will setup a mapping.
   1. Required fields are First Name, Last Name, Email and Company Name.
   2. Recommended fields are Company size and Industry, however we can add as many fields as you like.
3. In order to get access to your Marketo contacts through the API, we need 3 values:
   1. client ID
   2. client secret
   3. your Marketo API endpoint ID
4. To generate a new Client ID/secret, n Marketo admin needs to create a new API only user. Go to **Admin > Users & roles > Invite new user**
5. Fill out the form as described (the email address is just a placeholder so could be anything) and click Next
6. ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/608160b78996210f18bd5f85/file-hYnemiYJf5.png)
7. Select the API Role and make sure to tick the API Only option\
   ![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/60815cb53149d33a19c6f5f8/file-FXgvWisaiw.png)
8. Next, in the Marketo admin section, go to **Launchpoint > New > New service**
9. Fill in the new service form and select the API only user you created in the previous steps![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/608161703149d33a19c6f61c/file-bgbr0golja.png)
10. Once the service is created, click on **View details** and copy the client id and Client secret.![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/6081626ff8c0ef2d98df50e9/file-CzHid51vbq.png)
11. Copy these details&#x20;
12. Now the last step is to collect your Marketo API endpoint ID. This can be found by going to the web services section in the admin pannel and copy the REST API endpoint![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/608164d78af76a714bfd9d86/file-r43GFv9hpR.png)
13. Thats it, send us these 3 values and we can enable the integration.

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on April 22, 2021
