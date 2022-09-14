# Zapier webhook

In order to update Leads in LeadBoxer with data from other tools you can use the Zapier web-hooks feature.&#x20;

For reference, check out the technical documentation on how-to [Submit data to LeadBoxer by URL](https://docs.leadboxer.com/article/105-http-tracking-api)

Step One: setup your trigger with Zapier

Step Two: set-up Zapier web-hook as action with the GET option&#x20;

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fcf9670388c5a0089e64a72/file-hMqomeJeky.png" alt=""><figcaption></figcaption></figure>

Step Three: add the base url: eg

```url
https://log.leadboxer.com/?si=your-dataset-id&proxy=true
```

NOTE: you will need to 'build' the URL and add your key value pairs as parameters like this:&#x20;

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fcf978c12909d16116dfd7d/file-X8qXtRgkH1.png" alt=""><figcaption></figcaption></figure>

Step Four: Leave all other fields to their default value and test.

**If you do not provide a userID, we will try to merge the event with an existing user with the same email address.**

### Updating existing users where email is not known

If you would like to update existing 'Anonymous' users or leads, you need to provide the LeadBoxer user ID

You can get the LeadBoxer user ID by reading this from the Cookie, with the following javascript function:

```javascript
ot_uid();
```

Here is an example from the console&#x20;

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fcf91ae471dc000c9affe88/file-ECrBYNfd84.png" alt=""><figcaption></figcaption></figure>

You need to pass this user ID to webhook as a value for **uid** eg

```
uid = 1606468777834.459913894
```
