# Leadscore management

## How to change the leadscore

### Customise leadscore&#x20;

[![](https://gallery.mailchimp.com/bf6600641dcdb33445c8b6553/images/8710ca03-9097-409d-b8d1-46da82638995.png)](https://product.leadboxer.com/)

**Q: what does this mean in english?**

**A: you can influence how leads are scored.**

Adjusting your leadscore settings will change the way leads are prioritised and ranked, in terms of how your lead list is ordered. The leads that get the highest score will appear at the top of the list.

### How it works:

It is now possible to set weights on lead properties. In other words, you tell us what's important, and we weight it. These are the properties you can customise:

* email
* phone
* website
* LinkedIn match
* Chamber of Commerce (NL)
* company
* name
* industry focus

### Four simple steps to customise leadscores

Login to LeadBoxer, select 'Leadscore' from the drop-down, and:

1. **Select dataset** from dropdown
2. For each property **set a weight** on slider
3. **Add focus industries** (optional)
4. Click **Save**.

\


## Increase leadscore when key urls are visited

You can already  [change your leadscore](https://docs.leadboxer.com/article/83-video-how-to-adjust-leadscore). Now, we're adding more leadscore functionality. With this release, you can define which urls on your website have an impact on leadscore. In other words, leads qualify themselves by showing interest in important pages; pricing or specific product pages. This feature means that when leads visit the pages you tell us are important - they receive a higher leadscore, and come to the top of the list, and to your attention.

### Why is this important?

Receive 'buy signals' - leads who check key pages of your website are more likely to convert into customers. For example, If a lead checks your pricing page, he's a warmer lead than the average visitor. 'Buy signal' - behaviour signalling interest - changes from business to business and you need to pay attention to your key pages. Here are a few examples that we hope can help you generate more leads and close even more deals.

#### How to assign a single url

When you access your leadscore settings, scroll down until you see the item 4. There, you just need to define which URL is relevant and should affect your leadscore. You can use a absolute  url, like [http://www.mywebsite.com/sample-page](http://www.mywebsite.com/sample-page), or relative paths, like /sample-page/.Just write your url on the left, and assign a weight to it.![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5832e340c697916f5d053079/file-59ddEQyjIf.gif)\
Using relative paths to target multiple urlsIf you have multiple plans, and you want to check if the visitor visited any of the pages, you can use the url structure to achieve this. for example:&#x20;

* www.mywebsite.com/plans/plan-a
* www.mywebsite.com/plans/plan-b
* www.mywebsite.com/plans/plan-c

You can define your url as:

* www.mywebsite.com/plans/\*

This will catch everything that comes after 'plans'. So, in case you launch or test new plans in the future, you are covered.

### Adding multiple URLs

You can also add up to 5 different urls to your leadscore settings, assigning a different weight for each of them. Each url will count individually for your final leadscore calculation.

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5832e349903360645bfa69a8/file-mRjCbQdODx.gif)

That's it. Now  [login](https://product.leadboxer.com/) into your account and try it yourself.\
\




## Video: how to adjust leadscore

This short video piece will tell you how to adjust your leadscore, and explain why this is helpful.

{% embed url="https://youtu.be/lCvjw11_mMA" %}

\


## Leadscore parameters

If you want to use the leadscore features build inside our API you can use this documentation to get started.

The LeadBoxer scoring engine can score on 4 criteria

1. Range
2. Match
3. Exist
4. Boost

### Range

A range can be used for scoring on number ranges, eg pageviews, visits, etc.Range needs these 5 values:

1. field name
2. Start of the range
3. End of range
4. Score value
5. Comma (not for last)

**Example:**

user.total\_number\_visits.total\_number\_visits\_long|1|5|2.3,user.total\_number\_visits.total\_number\_visits\_long|5|25|4.7,user.total\_number\_visits.total\_number\_visits\_long|25|1000|7.0,user.total\_pages\_viewed.total\_pages\_viewed\_long|1|5|2.3,user.total\_pages\_viewed.total\_pages\_viewed\_long|5|25|4.7,user.total\_pages\_viewed.total\_pages\_viewed\_long|25|1000|

### Match

Match can be used if you want to score on a exact value match on any field

A match needs 3 values

1. field name
2. Value
3. Score

**Example**

OrganizationIndustry|Publishing|9|last\_country\_code|US|9

### Exist

Exist can be used to score on the existence of a value

An Exist needs 2 values

1. field name
2. Score

**Example**

email|3,organizationPhone|10,organizationDomain|15

### Boost

Boost can be used for scoring on events/pageviews/etcA Boost requires 3 values

1. Event type (usually root\_url)
2. The actual URL
3. Score

**Example**

root\_url|https://mydomain.com/contact/|7,root\_url|https://mydomain.com/buy-your-equipment/|7,root\_url|https://mydomain.com/sell-your-equipment/|7
