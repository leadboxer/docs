# Active Campaign

This integration can be used to push LeadBoxer data to Active Campaign.

The main functionality is to enrich and update your Active Campaign Contacts and Accounts with data available in LeadBoxer.

The integration also pushes the captured behaviour for each lead into a Contact widget.

The data can also be used to create Automations. For example to tag a contact if they visit a certain page, come from a specific campaign, or if an account has a specific industry, etc.





{% hint style="info" %}
Currently we only support Leads that have been identified with an email address, eg existing contacts. To identify your contacts learn more here: sadsa
{% endhint %}

#### The data flow / logic

* Every hour we will check for a specific segment if there are any new leads or contacts and /or activity.
* Once we find new data, we will create or update existing contacts and linked accounts (organizations)
* Both Contacts and Accounts will be enriched with pre-defined fields, if present in LeadBoxer
* For contacts, a 'LeadBoxer Events' widget will be added, which will include the events or pageviews measured by LeadBoxer
*

### Setup the Integration

#### Preparations:&#x20;

* You need to be both an admin in LeadBoxer as in Active Campaign
* Define the Segment that contain the contacts you want to sync to Active Campaign



#### Step 1.

Provide the basic details such as&#x20;

* The name of the integration. This is particular useful if you plan to add multiple integrations
* The subdomain value of your AC account
* the API key, you can find this under Settings > developer
* The dataset or site in LeadBoxer you want to integrate with &#x20;
* the Segment that you want to use as source.

<figure><img src="../../.gitbook/assets/Notification_Center.png" alt=""><figcaption></figcaption></figure>

Step 2.

Define who will be the 'owner' of the newly created Contacts and Accounts in Active Campaign.

<figure><img src="../../.gitbook/assets/LeadBoxer_App.png" alt=""><figcaption></figcaption></figure>

Contact fields added and populated by LeadBoxer

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
*

