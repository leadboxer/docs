# Copernica

### Identify & track Copernica email recipients on your website&#x20;

The LeadBoxer Copernica Integration automatically pulls all activity from your Copernica account into LeadBoxer, This means that all recipients who either a) read your emails or b) click on a link, will be created or updated in LeadBoxer. These leads will also be enriched and scored. Using Segmentation and notifications you can automatically find out who is interested in what and if they are Ready-to-Buy.

NOTE: To enable the Integration you need to provide us with a Copernica API token. We will only use this to pull / retrieve (read) the behavior of your Copernica audience.

### How to enable

**Step 1: Connect LeadBoxer with Copernica**&#x20;

To get started, login to your Copernica account (as admin) and register a new app. You can do so by using the registration form on [the dashboard](https://www.copernica.com/en/applications) of the Copernica website. After completing this registration you can find another form on the dashboard that allows you to link one or multiple accounts.

After you've registered your application and have linked it to your account, you will get access to the API token. This is a long string of alphanumeric characters

Once you have an API token, go to LeadBoxer (as Admin) browse to the integrations pages, paste the token in the token area.

If you have multiple websites or datasets in your LeadBoxer account, you can choose the default dataset you want your data to go. if you run multiple campaigns for multiple websites, you can route the data based on the sending domain.

Save the key and you are all set.

LeadBoxer will now start pulling in the data going forward.

#### Step 2: Connecting website activity with your Copernica audience

As you may know, LeadBoxer can also track all activities or behaviour from your website visitors, and in order to make the connection between your email audience and your website visitors you need to pass the Copernica contact ID so that we can connect the two. The ID should be added as a parameter to the URL of the landing pages and will allow us to identify the website visitor.

Copernica has this great feature that allows you to append all links with additional parameters in your templates, so to enable this simply go to 'Extend hyperlinks' from the dropdown in your template view and add these parameters to all your links going to your site:

```
lb_src=copernica
lb_eid={$profile.id}
```

\


<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5cdad7b90428634b85592fbf/file-BbOL6bSWLC.png" alt=""><figcaption></figcaption></figure>

Example:\


Thats all, and let the magic begin!
