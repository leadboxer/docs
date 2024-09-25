# Definitions & Glossary

## Definitions

### Leads

There are manifold definitions of what constitutes a 'lead'. We don't think it matters - as long as the definition is clear and fixed across an organisation with regards to marketing and sales workflows.

Additionally there are multiple subsets of Leads such as Marketing Qualified Leads (MQL), Sales Qualified Leads (SQL), BAND leads, hot leads, etc.

#### Our definition of a Lead:

{% hint style="success" %}
In LeadBoxer, we have defined a **Lead** quite broadly as (1) any <mark style="color:orange;">**Individual**</mark> that shows or has shown any interest in your product or service AND (2) is identifiable as either an (anonymous) employee of a company or as a know contact.
{% endhint %}

***

### Accounts

In LeadBoxer, we define companies and organizations as <mark style="color:purple;">**Accounts**</mark>. Accounts contain one or more leads. In other words:

{% hint style="success" %}
**An account is a grouped 'view' of leads from the same organization.**
{% endhint %}

***

### Events (pageviews)

An event in LeadBoxer is defined as any tracked activity that takes place on an internet-connected device.&#x20;

{% hint style="info" %}
Example events include: pageview, (email) clicks, swipe, scroll, download, email open, etc.
{% endhint %}

***

### Sessions (website visits)

A Session begins when a Website visitors enters your site with an entry event and views a succession of one or more pages. Each page requested and viewed is a pageview. The end of a visit is signalled by an exit event or a 10-minute period of inactivity. In that case, a next event (click) will start a new visit.

### Behaviour tracking

By using various tracking technologies and connecting with your other marketing tools, we can (among other things) track individual leads when they browse your site and read your emails. In other words, LeadBoxer can track all the (digital) interactions or engagement your leads have with your content or organization and store this as their 'behaviour'. This behaviour can be found for each Lead as part of their LeadProfile&#x20;

{% hint style="info" %}
Individual behavioural visualisation is also know as a click-stream, event-stream, action-stream, etc.
{% endhint %}

The behaviour (a) gives insight into lead interests, buyer journey, marketing phase, and (b) provides input to build up a rich Lead Profile, for example by [tagging](elements/lead-tags.md) based on pages they visit.

### Clickstream

A clickstream, or click path, is a list of all the events registered from a lead, presented in the order the events were registered, also defined as the ’succession of pageviews’ that each Lead makes through a website.

### Leadscore

A Leadscore is method to calculate the interest or value of lead by setting weights on selected properties and behaviour. In other words, you tell us what's important, and we weight it.&#x20;

The end result is a number from 0-100 where higher means better.

### **s. e. = single event (visit)**

A “single event” visit is defined when a lead or visitor views a single page of your site, and no second event was registered.

## Glossary & field names

### Person or contact fields

<table><thead><tr><th width="251">Field Name</th><th>Technical name</th></tr></thead><tbody><tr><td>First Name</td><td>firstName</td></tr><tr><td>Last Name</td><td>lastName</td></tr><tr><td>Full Name</td><td>fullName</td></tr><tr><td>Job Title</td><td>title</td></tr><tr><td>Email Address</td><td>email</td></tr><tr><td>Lead Tag</td><td>leadTag</td></tr><tr><td>Account Tag</td><td>accountTag</td></tr></tbody></table>

LeadBoxer captures various marketing data and stores these in the following fields:

### Acquisition fields

{% hint style="info" %}
Note: Each of these fields has both a **first** and **last** version.&#x20;

* First represents the very first value that was tracked. eg the initial campaign.  This field will never be overwritten.
* Last represents the very last value that was tracked & stored. this value will be overwritten every time we track or receive a new value.
{% endhint %}

<table><thead><tr><th width="219">name</th><th>description</th></tr></thead><tbody><tr><td>Channel (First)</td><td>A channel is a marketing term that refers to the source of traffic to a website or a specific page within a website. Common channels include organic search, social media, email marketing, and paid advertising. See <a href="../integrations/website/tracking-marketing-campaign-data-utm-tags.md#channels">Tracking Marketing campaign data</a> for more details.</td></tr><tr><td>Channel (Last)</td><td>We keep track of both the first and last channel of each Lead.</td></tr><tr><td>Campaign (utm)</td><td>This is the name of the campaign that the traffic is associated with, eg "Spring sale"</td></tr><tr><td>Source (utm)</td><td>This indicates the source of the traffic. eg "google"</td></tr><tr><td>Medium (utm)</td><td>This indicates the medium through which the traffic was acquired, eg "cpc", "email", etc.</td></tr><tr><td>Content (utm)</td><td>This field is often used to differentiate between different versions or elements of an ad or a piece of content.</td></tr><tr><td>Term (utm)</td><td>This field is used to track the specific keywords or search terms that were used to trigger an ad or a piece of content. It is commonly used in paid search campaigns to track the effectiveness of specific keywords or phrases.</td></tr><tr><td>Referrer</td><td>Third party website or source (i.e. search engine, link, ad, email) through which a visitor reaches your site. Search engines are the primary example. All sites with links leading to your site are also referrers.  Email and newsletters can also be referrers.</td></tr><tr><td>Referring domain</td><td>the Top Level Domain of a referrer (eg google.com)</td></tr></tbody></table>



### Behavioural

<table><thead><tr><th width="236"></th><th></th></tr></thead><tbody><tr><td>landing Page (title)<br><mark style="color:blue;">[string]</mark></td><td>Our Landing page values are simply the first page the lead lands on and will not be overwritten if the user visits again.<br>We do store this value also on the session level, and this data is available via the API </td></tr><tr><td>landing URL <br><mark style="color:blue;">[url]</mark></td><td>The Landing URL is the full URL of the landing page</td></tr><tr><td>exit page<br><mark style="color:blue;">[url]</mark></td><td>The last page a visitor views before leaving your site. If the visitor follows a link from your site LeadBoxer will record the exit link followed. If they close their browser or use bookmarks no further information on their activity is available.</td></tr><tr><td>exit link<br><mark style="color:blue;">[url]</mark></td><td>An exit link is a link from your site (domain) to another site (technically a 3rd party domain). An exit link is a link leaving your site to third-party site, a bridge from your site to another. Exit links begin on your site and lead to the other side of the bridge.</td></tr><tr><td>event count<br><mark style="color:blue;">[number]</mark></td><td>Event; pageview, click, download, login, newsletter open, etc. Any activity that takes place on an Internet-connected device can be defined as an <strong>event</strong>. </td></tr><tr><td>web visits<br><mark style="color:purple;">Total / This Period</mark><br><mark style="color:blue;">[number]</mark></td><td>The total number of distinct web visits (sessions) made to a site or the subtotal over a given period of time. <br>A session starts with an entry event and ends with an exit event or a 10 minute period of inactivity. A visitor can make an unlimited number of visits. Also know as web sessions. </td></tr><tr><td>events<br><mark style="color:purple;">Total / This Period</mark><br><mark style="color:blue;">[number]</mark></td><td>The total number of distinct events measured or the subtotal over a given period of time. </td></tr><tr><td>last event <br><mark style="color:blue;">[dynamic]</mark> </td><td>The time difference between now and the last registered activity time by a user . eg 5s, 2 days, 3 weeks, or 4 months.</td></tr><tr><td>last event in date format<br><mark style="color:blue;">[date]</mark> </td><td>The last registered activity time in ISO date format</td></tr></tbody></table>

### Technical

| field name  | Technical Name                                    |
| ----------- | ------------------------------------------------- |
| Browser     | last\_browser                                     |
| Platform    | last\_platform                                    |
| Screen size | last\_resolution\_height, last\_resolution\_width |

### Geo Location

We determine an internet visitor’s location based on their IP address and /or GPS coordinates. ​Geolocation is the identification of the real-world geographic location of an object, such as a mobile phone or an internet-connected computer.&#x20;

<table><thead><tr><th width="235"></th><th></th></tr></thead><tbody><tr><td>person city </td><td>The city where the IP address is registered </td></tr><tr><td>person country </td><td>The country where the IP address is registered</td></tr><tr><td>person region</td><td>The region where the IP address is registered</td></tr><tr><td>IP address</td><td>The last IP address of the visitor or Lead </td></tr><tr><td>ISP</td><td>The last IP address of the visitor or Lead </td></tr></tbody></table>



### Organization fields

LeadBoxer offers multiple options for identifying organizations and companies. Examples are via IP address, login, sign-up, email or form submission.

Once we have identified an organization, we enrich this identified organization with an extensive range of fields. As we use multiple data sources, field availability differs, depending on factors such as region, location, online presence, etc.

<table><thead><tr><th width="144">Description</th><th width="264">field name</th><th>technical name</th></tr></thead><tbody><tr><td><strong>Name</strong></td><td>Organization Name</td><td>organizationName</td></tr><tr><td><p><strong>Address fields</strong><br><br></p><p><br><br><br><br><br><br><br></p></td><td><p>Street Name</p><p>Street Number</p><p>SubPremise</p><p>City</p><p>PostalCode</p><p>State</p><p>StateCode</p><p>Country</p><p>CountryCode</p><p>Longitude</p><p>Latitude</p></td><td><p>organizationStreetName</p><p>organizationStreetNumber</p><p>organizationSubPremise</p><p>organizationCity</p><p>organizationPostalCode</p><p>organizationState</p><p>organizationStateCode</p><p>organizationCountry</p><p>organizationCountryCode</p><p>organizationLongitude</p><p>organizationLatitude</p></td></tr><tr><td>Generic fields<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br></td><td><p>Logo </p><p>Employee Count Estimate</p><p>Employee Count Range Code</p><p>Employee Count Range Name</p><p>Industry Name </p><p>Industry Code</p><p>Industry Local Code</p><p>Industry Group </p><p>Naics Code </p><p>Sector </p><p>Tags </p><p>Specialties </p><p>Founded </p><p>Description </p><p>Description Short </p><p>Type </p><p>Domain </p><p>Phone </p><p>Email Addresses  </p><p>Ceo Title </p><p>Executives </p><p>NationalId </p><p>Technology </p><p>Website Ip Address</p></td><td><p>OrganizationLogo</p><p>organizationEmployeeCountEstimate</p><p>organizationEmployeeCountRangeCode</p><p>organizationEmployeeCountRangeName</p><p>organizationIndustryName</p><p>organizationIndustryCode</p><p>organizationIndustryLocalCode</p><p>organizationIndustryGroup</p><p>organizationNaicsCode</p><p>organizationSector </p><p>organizationTags</p><p>organizationSpecialties organizationFounded organizationDescription organizationDescriptionShort organizationType</p><p>organizationDomain</p><p>organizationPhone organizationEmailAddresses  organizationCeoTitle organizationExecutives organizationNationalId organizationTechnology organizationWebsiteIpAddress</p></td></tr><tr><td>Social fields<br><br><br><br><br><br></td><td><p>LinkedIn ID </p><p>LinkedIn Url </p><p>Facebook Url </p><p>Twitter Url </p><p>Instagram Url </p><p>Youtube Url </p><p>Google Places Id</p></td><td>organizationLinkedInID organizationLinkedInUrl organizationFacebookUrl organizationTwitterUrl organizationInstagramUrl organizationYoutubeUrl organizationGooglePlacesId</td></tr><tr><td>Financial</td><td>Sales Volume Category Name<br>Sales Volume Currency<br>Sales Volume Category Code</td><td>organizationSalesVolumeCategoryName organizationSalesVolumeCurrency organizationSalesVolumeCategoryCode</td></tr></tbody></table>
