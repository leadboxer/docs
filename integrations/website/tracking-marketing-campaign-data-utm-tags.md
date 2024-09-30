# Tracking marketing campaign data (UTM tags)

## What are UTM tags?

UTM tags, or Urchin Tracking Module tags, are parameters added to the end of a URL that track the source, medium, and campaign name of website traffic. These tags are used by marketers to track the effectiveness of different marketing campaigns and channels.

Here is an example of a URL with UTM tags:

```url
https://example.com/?utm_source=google&utm_medium=cpc&utm_campaign=spring_sale
```

In this example, the UTM tags are:

* **utm\_source=google**: This indicates the source of the traffic, which in this case is Google.
* **utm\_medium=cpc**: This indicates the medium through which the traffic was acquired, which in this case is cost-per-click advertising.
* **utm\_campaign=spring\_sale**: This is the name of the campaign that the traffic is associated with, in this case, a spring sale.

UTM tags allow marketers to track the effectiveness of their campaigns and channels by providing data on how much traffic each campaign is driving, what sources the traffic is coming from, and what mediums are most effective for generating traffic. This information can be used to optimize campaigns and allocate resources more effectively.

There are actually 5 different kind of UTM tags, but these 2 are used less often and are optional:

* **utm\_term=search-term**: This parameter is used to track the specific keywords or search terms that were used to trigger an ad or a piece of content. It is commonly used in paid search campaigns to track the effectiveness of specific keywords or phrases.
* **utm\_content=buy\_now\_button**: This parameter is used to differentiate between different versions or elements of an ad or a piece of content. It can be used to track which version of an ad or email is generating the most clicks or conversions.

### UTM tags and LeadBoxer&#x20;

LeadBoxer automatically captures all the UTM tag values for each session or pageview, and saves these for each Lead as both **First \*** and **Last \*** values you can find them in each Lead Profile under the Acquisition section. You can also see them in the [Leads & Accounts](../../fundamentals/projects.md) overview.

{% hint style="success" %}
We highly recommend you set up UTM tags for each of your campaigns and add them to the URLs that you use for each campaign.&#x20;
{% endhint %}

The data is very valuable for Marketing teams and can be used to answer various questions. For example:

* identify which campaign or source or medium brings in the best leads &#x20;
* For each lead, see what was the initial source or marketing campaign

### Attribution & Conversion

UTM tags can help to attribute different sources and campaigns to a conversion by tracking the source, medium, campaign name, and other parameters associated with each click on a website, landing page, email open, etc.

If you are running multiple campaigns to drive traffic to your website, for example a Facebook campaign, a Google Ads campaign, but also an email marketing or nurturing campaign, there is a high probability that your leads will have multiple and different UTM values for each time they interact with your content.&#x20;

So how will you know which campaign can be attributed to an actual conversion?

At LeadBoxer, we support both the First and Last click attribution model, and allow for you to capture and store the UTM values for the actual session where a conversion has taken place using [Workflow Automation](../../fundamentals/elements/workflow-automation.md#actions)



## Channels

UTM tags are also used (amongst other things) to define a channel through which traffic is acquired. A channel is a marketing term that refers to the source of traffic to a website or a specific page within a website. Channels include:

direct, organic, social, email, referral and paid.

For Paid Leads, we Support the following landing page parameters:

* Google: `gclid`
* Tiktok: `ttclid`
* Microsoft Bing: `msclkid`&#x20;
* X /  Twitter: `twclid`&#x20;
* Doubleclick: `dclid`&#x20;
* Yahoo: `yclid`

Alternatively, you can also use the UTM parameter medium. When this is set to `cpc`, `ppc` or  `paidsearch` we will automatically set the channel to paid.

***

We support First and Last Channel, meaning we store the channel used for the first session /visit and the last session / visit.

Channels values can be found in the Lead & Accounts overview, in any Lead Details and can also be used as a [Filter](../../fundamentals/elements/filters.md).





## Howto: Create UTM Parameters for Your pages

The simplest way to create UTM parameters for your links is by using the  [Google Analytics URL Builder](http://www.google.com/support/analytics/bin/answer.py?answer=55578). This page also has some helpful hints on how to use the different UTM parameters.

* **Campaign Source** (utm\_source) – Required parameter to identify the source of your traffic such as: search engine, newsletter, or other referral.
* **Campaign Medium** (utm\_medium) – Required parameter to identify the medium the link was used upon ie. : email, CPC, or other method of sharing.
* **Campaign Name** (utm\_campaign) – Required parameter to identify a specific product promotion or strategic campaign such as a Spring Sale or other promotion.
* **Campaign Term** (utm\_term) – Optional parameter suggested for paid search to identify keywords for your ad.&#x20;
* **Campaign Content** (utm\_content) – Optional parameter for additional details for A/B testing and content-targeted ads.

You can learn more about  [how to tag your links](https://support.google.com/analytics/answer/1033867) in Google Analytics Help. It also contains a handy chart view with an example of one campaign with different sources & mediums.

Note that UTM parameters are case sensitive, which means if you use  _abc_ for your utm\_campaign tags on some links and _ABC_ for your utm\_campaign tags on other links, they will show up as separate campaigns. Also note that UTM parameters will be shown in the browser’s address bar, so be sure you’re not using any tags that you would want to remain unseen.



**Additional reading:**

{% embed url="https://mailchimp.com/resources/utm-links/" %}

{% embed url="https://web.utm.io/blog/utm-naming-conventions-guide/" %}
