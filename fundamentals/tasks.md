# LeadBoard

## What is the LeadBoxer LeadBoard

The LeadBoard is a [kanban](https://en.wikipedia.org/wiki/Kanban)-style overview of your Leads & Accounts, where you can qualify, annotate, investigate, and manage your leads. It allows you to keep track of your most important Leads and their journey towards Sales opportunities and eventually new customers.

The concept is not super complicated (that is the beauty of it) and you might already be familiar with it as many tools already have used the concept, the most well-known tool is Trello.

<figure><img src="../.gitbook/assets/wat_is_kanban_.png" alt=""><figcaption><p>The basic Kanban board</p></figcaption></figure>

In our case, we have applied the concept so that each 'card' on your LeadBoard represents a Lead or Account. The natural flow is that your cards or Leads move from left tot right as they travel through your marketing workflow or funnel.&#x20;

<figure><img src="../.gitbook/assets/LeadBoxer_App.png" alt=""><figcaption><p>The LeadBoxer LeadBoard</p></figcaption></figure>

The final step in your LeadBoard should be the step in your workflow where you offer or handover the Lead to Sales, and basically saying that you think this Lead is ready to be contacted, ready to be closed, ready to buy, or basically anything.

## Getting started

If you arrive at the LeadBoard for the first time, you get asked to create your first LeadBoard.

{% hint style="info" %}
1. Before you continue, we recommend you make sure you have workflow defined: eg a marketing funnel, lead generation or lead qualification workflow.&#x20;
2. Also you first need to create a Segment that contains the Leads you want to be imported into your boards.&#x20;
{% endhint %}

To create a LeadBoard, you click on the 'Create LeadBoard' button and follow these 3 steps to complete:

1. Create LeadBoard
2. Define Stages
3. Import Data

### 1. Create New LeadBoard

There are 4 items we need to create a LeadBoard.

<figure><img src="../.gitbook/assets/LeadBoxer_App (1).png" alt=""><figcaption><p>Step 1 of Create new LeadBoard wizard</p></figcaption></figure>

* Provide a name for your LeadBoard. We recommend a short and descriptive name, so that all users understand what the goal of the board is. eg. Demo signups, LinkedIn campaign leads, EU Leads, etc.
* Select the Dataset / site.&#x20;
* Select the [Segment](elements/task-lists.md) from which the matched leads will be automatically imported in this LeadBoard.
* Set the visibility of this LeadBoard to be visible to only you or anyone that has access to this dataset.
* Click Next

### 2. Define stages

Based on you internal marketing workflow, add the stages so that your LeadBoard matches the steps you have defined to qualify or manage your leads. If you have not done this yet, we recommend you read this tutorial first: Define Your Marketing Workflow.&#x20;

<figure><img src="../.gitbook/assets/LeadBoxer_App (2).png" alt=""><figcaption><p>Step 2 of Create new LeadBoard wizard</p></figcaption></figure>

* For each workflow step, add a Stage and provide a descriptive name
* Once all steps are defined, make sure they are in the right order (you can drag & drop to change the order)&#x20;
* Check if the default column is the 'entry' stage. This is the stage where leads will be added by either the auto import or manually.
* Click Next

{% hint style="info" %}
We recommend to to start simple, with a minimum of 3 stages. You can always revisit and modify if needed later.&#x20;
{% endhint %}

### 3. Import Leads

Now that you have created your LeadBoard and defined the stages, you can start managing your leads right away by importing your existing LeadBoxer leads into your new LeadBoard.

<figure><img src="../.gitbook/assets/Notification_Center.png" alt=""><figcaption><p>Step 3 of Create new LeadBoard wizard</p></figcaption></figure>

You can choose data from today, last 7 days or last 14 days.

Click import, to perform this step or skip and start with a clean LeadBoard.

## Using the LeadBoard

Once you have Leads showing up in your default or entry stage, the high-level goal is that you  move as much cards from left to right, if they are allowed to be moved according to your workflow.&#x20;

{% hint style="info" %}
We recommend that all movement of cards should be based on your defined marketing or Lead Gen workflow. If you havent defined this yet, we recommend you create one first.&#x20;
{% endhint %}

To see if a lead is qualified to go to the next step, you can analyze the data collected, which you can see by clicking on an individual Leadcard and open the so called Account Pannel.

### Manually adding Leads to the Leadboard

You manually add leads to the board by providing the domain name of the organisation or company. Our enrichment engine will try and find the associated firmographic details and once accepted the lead will show up in the default or entry stage.

## The Account Pannel

This Pannel shows up when you click on a Leadcard in your LeadBoard and provides you with an overview of all details from a company or organisation we call [Accounts](projects.md#what-are-accounts) and consist of 2 sections:

1. The Account details
2. The Lead details

### Account details

The Account details section on the Account Pannel shows the (enriched) company or organization information that is available based on the domain-name of the organisation.

### Lead details

The Lead details section shows a list of individual leads (or contacts) with some lead details such as marketing channel, sessions, events, etc. You can click on any Lead to expand this lead. this will reveal the last 5 session and their complete behaviour or clickstream. You can continue clicking to reveal 5 more sessions.&#x20;

#### &#x20;The Behavioural stream&#x20;

This subsection of an individual lead or contact contains the sessions and all the 'events' or actions that were tracked or registered within these sessions.&#x20;

Sessions are usually a group of events. and there are several kind of events that we automatically detect:

* pageview
* referrer
* exit&#x20;
* email open
* email click



#### Background Lead Operations

While you are successfully managing your leads in your LeadBoard(s), your Leads are not sitting still and perform all kinds of behaviour. To make sure this behaviour is reflected on your LeadBoard, we are checking each lead in your LeadBoard every hour and update the details if necessary.

&#x20;

