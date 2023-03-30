# Active Campaign

This integration can be used to push LeadBoxer data into Active Campaign.

The main functionality is to enrich and update your Active Campaign Contacts and Accounts with data available in LeadBoxer.

The integration also pushes the captured behaviour for each lead into a Contact widget.

Integration also contains an event trigger, meaning behavioural data can also be used to create Automations. For example to tag a contact if they visit a certain page, or  arrive from a specific campaign, etc.



{% hint style="info" %}
Currently we only support Leads that have been identified with an email address, eg existing contacts. To identify your contacts on your site, [track your forms](../website/manual-form-tracking.md) or connect your [email applications](../email/).
{% endhint %}



For a technical overview of this integration, see [here](active-campaign.md#technical-overview).

## How to Setup the Integration

#### Preparations:&#x20;

* You need to be both an admin in both LeadBoxer and Active Campaign
* Make sure you have created a [Segment ](../../fundamentals/elements/segments.md)that contains the contacts you want to sync to Active Campaign

#### Step 1.

On the integrations page (in the new Interface), go to the Active Campaign option and click New Integration

Provide basic details such as:

* The name of the integration. This is very useful if you plan to add multiple integrations
* The subdomain value of your AC account
* the API key; you can find this under Settings > developer
* The [dataset](../../fundamentals/elements/datasets.md) or site in LeadBoxer you want to integrate with &#x20;
* the [Segment](../../fundamentals/elements/segments.md) that you want to use as source.

<figure><img src="../../.gitbook/assets/Notification_Center (1).png" alt=""><figcaption></figcaption></figure>

#### Step 2.

Define who will be the 'owner' of the newly created Contacts and Accounts in Active Campaign.

<figure><img src="../../.gitbook/assets/LeadBoxer_App (1) (4).png" alt=""><figcaption></figcaption></figure>

#### Step 3.

Select whether to import the last hour's data or not.

<figure><img src="../../.gitbook/assets/LeadBoxer_App (2) (2).png" alt=""><figcaption></figcaption></figure>

That's it! Once finished we will start updating every hour, on the hour.

### Technical overview

#### The data flow / logic

* Every hour we will check for a specific [segment](../../fundamentals/elements/segments.md) - if there are any new leads or contacts and /or activity.
* When we find new data, we will create or update existing contacts and linked accounts (organizations)
* Both Contacts and Accounts will be enriched with pre-defined fields, if they have a value present in LeadBoxer
* For contacts, a 'LeadBoxer Events' widget will be added, which will include the events or pageviews measured by LeadBoxer
* A new tag will be created and added to each Lead or Account that is created or updated by the integration
* A new List called 'LeadBoxer' will be created&#x20;



Custom fields for Contacts that are added and populated by LeadBoxer

* First Campaign&#x20;
* First Medium&#x20;
* First Source&#x20;
* First Term&#x20;
* First Content&#x20;
* Last Campaign&#x20;
* Last Medium&#x20;
* Last Source&#x20;
* Last Term&#x20;
* Last Content&#x20;

Contact fields mapped to LeadBoxer fields

* Email
* FirstName
* LastName
* Phone
* Job title

Account fields mapped to LeadBoxer fields

* Name
* URL
* Address 1
* City
* State
* Country
* Phone
* Number of Employees
* Description
* Annual Revenue



