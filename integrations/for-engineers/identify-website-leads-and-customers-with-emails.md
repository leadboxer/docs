# Identify website leads and customers with emails

### Track clicks within emails

Similar to email open events, tracking who clicks on a link in the mailings or newsletters you send, and which link they clicked on, can often be retrieved from the tool or solution you are using. However, most marketeers hardly look at this data, which is often forgotten as they focus on metrics such as open and click rates.&#x20;

LeadBoxer offers a different approach by tracking in-email clicks, and adding them to the (existing) lead or customer journey or clickstream. The benefit is that you will then know (exactly) what catches the attention of your audience and leads, and can respond directly.

Adding email link tracking is easy and the benefits are significant!

### Identify website leads & customers by email&#x20;

By tracking email clicks, there is another major benefit created:  if your email, or newsletter recipients click on a link to your website, you can pass all the information you have in your email database for this person and add or update their profile in LeadBoxer automatically.

Even more bonus: As we track leads and customer over longer periods of time, an identification through email can be applied to them retroactively, meaning : Once clicked through via email, leads or customers are identified for all past present and future behaviour.&#x20;

### How to Track Clicks and Identify website visitors with email

By adding the following parameters to the links in your email, you can enable this feature.

Create your mail campaign like you always do, and make sure you add links to a landing page. The landing pages will automatically capture the information being sent from the email or newsletter once they click a link.

When your email is ready, modify your link(s) and add custom parameters to the links. These parameters, known as '**merge tags**', will be added to your links

#### What is a Merge Tag?

In order to use newsletter or email tracking and connect email and web behaviour, we need a way to identify your recipients once they land on your site. We do this by way of a merge tag.

Dependent on the mailing software you use, merge tags may also be known as 'personalization fields', 'substitution strings', or 'personalization tags'. These tags allow you to insert data from your mailing list directly into your email campaigns. For example, if you are a MailChimp user and you’d like to insert your subscriber’s first name into your email, you might use the merge tag  \*|FNAME|\*. Every time MailChimp sees the tag \*|FNAME|\* in your email, they will replace this tag with the unique data associated with each recipient in your list.

Each Email Service Provider (ESP) or mailing platform has a slightly different way of handling these tags, which is why we ask that you choose from below table of common tags. By correctly identifying the merge tag for your mailing platform, you’re ensuring that LeadBoxer can collect all the data you’re looking for and match it back to the subscribers on your list.

When you include an email merge tag, this tells your ESP to insert your recipient’s email address in the link, which will pass us the amazing data you’re looking for.

#### Implementing Merge Tags

By adding Merge tag values to the link of your landing pages, we can grab these values and add them to the visitor, lead or customer profile.

We have implemented a couple of default parameters that you can populate with merge tags from your email database:

* email
* firstName
* lastName
* company
* phoneNumber
* lb\_id

Meaning you would need to append these to the links in your newsletter or email campaign.

eg

```
?email=*|EMAIL|*
```

This will append the email address of your recipient to the url of the landing page.&#x20;

You can do this for other fields available in your mail or newsletter solution. eg:

```
?email=*|EMAIL|*&firstName=*|FNAME|*&lastName=*|LNAME|*
```

Apply this to all links that link to your site, or the pages where our tracking pixel is implemented.

Save your newsletter, and test the links by clicking on them in the preview, you should see the email address and other fields appended to the url on your landing page. The following image shows what you should see appended to the url of your landing page:

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/615474a600c03d672075badf/file-S9d2KyFeoH.png)

### Campaign data (UTM tags)&#x20;

We also auto-capture campaign data tags, aka UTM tags.

[Read more on how we auto capture UTM tags](https://docs.leadboxer.com/article/10-tracking-utm-tags)

If an url has the following parameter in the URL of a landingspage: **utm\_medium=email** we will reder a the event in our interface as an 'email click', &#x20;
