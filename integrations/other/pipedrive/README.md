# Pipedrive

### Synchronise web & email activity with Pipedrive Leads, Deals, Persons and Companies

Identify and collect information about your leads & customers during their entire online buyer journey, and turn this data into actionable insights.&#x20;

In other words, LeadBoxer collects your website and email or newsletter data to automatically identify, enrich, segment, and score leads & customers based on their behavior and profile data.

#### Leads Integration workflow:

1. Let LeadBoxer identify **organizations**, (and/or persons) on your website using IP lookup, newsletters, email, forms, signups, logins, etc
2. Create and define a segment in LeadBoxer with leads that you want to be pushed to Pipedrive as Leads.
3. Setup the integration (see below)
4. Results: We will create new Pipedrive Leads for each LeadBoxer lead that is in the selected LeadBoxer segment
5. Actioned!

#### Deals Integration workflow:

1. Let LeadBoxer Identify **persons** on your website using newsletters, email, forms, signups, logins, etc.
2. Create and define the segment with leads (or customers) you want to synchronise with Pipedrive
3. Setup the integration (see below)
4. Result: We will push all activity from leads this segment to Pipedrive and update existing Deals, Persons and Companies. Optionally we can create new deals if we cannot find any in a pipeline of your choice.&#x20;
5. Actioned!

### **Setup and installation**

1. If you haven't already done so, go to [https://www.leadboxer.com/](https://www.leadboxer.com/) and create your (free) trial account
2. Install the tracking pixel on your site
3. Implement either form tacking, newsletter tracking or use the gmail or Outlook plugins.
4.  **For Pipedrive Leads:**\
    In the LeadBoxer app, create and define a new segment containing the leads you want to push to Pipedrive. You can use all the filters to make sure only qualified leads are actually pushed to Pipedrive.

    Pipedrive has not yet added the Leads integration into their authentication workflow, so for the leads integration you will need to add your Pipedrive API key. (instructions on [obtaining your API key](https://support.pipedrive.com/hc/en-us/articles/207344545-How-can-I-find-my-personal-API-key-))\
    \

5. **For Deals, persons, organizations:**\
   In the LeadBoxer app, create and define a new segment containing the leads or customers you want to push to Pipedrive. We will push all behavioral events from Leads in this segment to Pipedrive as activities.
6. In Pipedrive (you need to be Admin): Activate the [LeadBoxer App in the Pipedrive marketplace](https://marketplace.pipedrive.com/app/lead-boxer/416e3a6f032c2d02), this will redirect you to the LeadBoxer integrations page.
7. On the integrations page:&#x20;
   1. For Leads\
      Select a) the dataset you want to sync, b) the segment to use c) if you prefer that we create Leads that linked to organizations or to persons, or both. Note: for persons, an email value needs to be known.
   2. For Deal, Person and Organization activities:\
      Select a) the dataset you want to sync, b) the segment to use\
      Optionally, you can select the default pipeline you want us to create deals in\
      Note: an email value needs to be known for us to find and update the deals/ persons/ organizations.
   3. Save.

\


<figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5fa666e446e0fb0017fc9bf9/file-NxjfHpyMjj.png" alt=""><figcaption></figcaption></figure>

We advise to test with a small number of leads inside your segment and use a test pipeline before you save.

Once saved, we will automatically start pushing all web & email activity to Pipedrive

### Background info for Pipedrive Leads integration

###

**Technical Logic:**

With sync option set to Organization: we search for the organisation and person. If the organization exists, we link the lead to this organization. If the organization does not exist we create a new organization.

With sync option set to Person: we search for the person. If the person exists, we link the lead to this person. If the person does not exist we create a new person.

With sync option set to Both: We search for the organisation and person, if the organization exists, we link the lead to this organization, if the organization does not exist we create a new organization. We search for the person, if the person exists, we link the lead to this person, if the person does not exist we create a new person.

### Background info for Creating and Updating Pipedrive Deals, Persons and Companies

Our goal when building the Pipedrive Deal integration was to pass only qualified leads, and avoid polluting/ pushing noise into the pipelines/ CRM. Filling a pipeline with too many (unqualified) leads is counter-productive.

For that reason we engineered the following push logic:

1. We only send data to Pipedrive for leads/ customers that have been identified by email
2. We only send data to Pipedrive from the leads that appear in the Segment you have defined in your setup
3. We send updates to Pipedrive hourly (on the hour)

**Technical Logic:**

We create an activity in Pipedrive and link this to:

Person: We do a lookup for a person using email as identifier. If the person exists, we link the activity to this person. If the person does not exist, a new person is created.

Company: We check if the person has a linked Company. If there is a organisation linked, we link the activity to this Company. If the Company does not exist, we will create a new Company and link it.

Deal: We check if the person has a linked Deal. If there is a Deal linked, we link the activity to this Deal. If the Deal does not exist, we will create a new Deal and link it.
