# Intro: Track Email Opens

### How to Track Email Opens or Reads

The ability to see who opens emails you send is not cutting-edge new technology, and is offered by many mailing or newsletter providers. What is new however, is the ability incorporate these events in the Customer Journey or clickstream of your online leads and customers. To support this we provide a pixel purpose-built for email tracking. You will need to add this pixel to your mailings or newsletters.&#x20;

#### The LeadBoxer Email Tracking Pixel&#x20;

Our tracking pixel is a transparent image with a size of 1x1 pixel, (hence the word pixel) that is loaded directly from our servers. By adding additional parameters to the URL of the image we can seamlessly pass data to the LeadBoxer servers.&#x20;

**AutoGenerate your email tracking pixel**

<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5abf3f16042863794fbeca16/file-KxSr9Uz4pD.png" alt=""><figcaption></figcaption></figure>

1. Log into LeadBoxer as admin and go to the datasets overview.&#x20;
2. Click the configuration icon next to the dataset/website you want to track and select email tracking pixel
3. Choose your mail/newsletter provider&#x20;
4. Enter a campaign name and the pixel is automatically generated.&#x20;

**Manual tracking configuration**

. The tracking pixel should look something like this:&#x20;

{% code overflow="wrap" %}
```html
<img src="https://track.leadboxer.com/log?datasetId={{yourDatasetId}}&campaign={{YourCampaignName}}&email={{emailMergTag}}">
```
{% endcode %}

There are 3 values that need to be modified:&#x20;

1. **datasetId** = this is the ID for the dataset or website you want to track email activity for&#x20;
2. **campaignName** = the name for your specific campaign&#x20;
3. **email** = the email address of the recipient. This needs to be dynamically populated by your mailing or newsletter program, using so-called **merge tags**&#x20;

#### What is a Merge Tag?

In order to use newsletter or email tracking to collect individual-level data on your subscriber behavior, we need a way to identify your subscribers in our tracking codes. We do this by way of a  **merge tag**.

Dependent on the mailing software you use, merge tags may also be known as 'personalization fields', 'substitution strings', or 'personalization tags'. These tags allow you to insert data from your mailing list directly into your email campaigns. For example, if you are a MailChimp user and you’d like to insert your subscriber’s first name into your email, you might use the merge tag  **\*|FNAME|\***. Every time MailChimp sees the tag \*|FNAME|\* in your email, they will replace this tag with the unique data associated with each recipient in your list.

Each Email Service Provider (ESP) or mailing platform has a slightly different way of handling these tags, which is why we ask that you choose from below table of common tags. By correctly identifying the merge tag for your mailing platform, you’re ensuring that LeadBoxer can collect all the data you’re looking for and match it back to the subscribers on your list.

When you insert the correct merge tag, this will tell your ESP to insert your recipient’s email address in our email tracking pixel, which lets us track the amazing data you’re looking for.

Merge tags differ per vendor/provider, below you will find the merge tags for some of the main email providers. If your vendor is not listed, please contact us.

| Email provider                                    | merge tag / variable name                |
| ------------------------------------------------- | ---------------------------------------- |
| MailChimp                                         | \*\|EMAIL\|\*                            |
| Sendgrid                                          | <p>[%email%]<br></p>                     |
| Intercom                                          | \{{ email \}}                            |
| ZOHO                                              | $\[EMAIL]$                               |
| Reply.io                                          | {Email}                                  |
| <p>Act-On<br></p>                                 | \{{E-mail Address\}}                     |
| ActiveCampaign                                    | %EMAIL%                                  |
| AWeber                                            | {!email}                                 |
| Campaign Monitor                                  | \[email]                                 |
| Drip                                              | \{{ subscriber.email \}}                 |
| Emma                                              | \[% member:email %]                      |
| GetResponse                                       | \[\[email]]                              |
| HubSpot                                           | \{{ contact.email \}}                    |
| Salesforce Marketing Cloud (formerly ExactTarget) | %%emailaddr%%                            |
| Pardot                                            | %%email%%                                |
| Marketo                                           | \{{lead.Email Address:default=noemail\}} |
| Constant Contact                                  | $Subscriber.Email                        |

#### Are There Any Limitations?

There are some known limitations to newsletter or email tracking.&#x20;

**Images need to be enabled**\
Since we rely upon an image loading, we aren’t able to track recipients who do not enable images for your email. Some email clients block external images, or are not capable of displaying HTML email, including older email clients or mobile devices. As a result these are not tracked and do not appear in your reports.

**Gmail**\
Gmail loads images via a proxy and cache. This means that using images to identify the recipient’s location and browser details won’t work. Since the images are cached, all subsequent opens won’t be trackable.

People using alternative clients to access their Gmail accounts will bypass Google’s image proxy.
