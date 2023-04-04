# Workflow Automation

At LeadBoxer we don't like to do a lot of repetitive tasks and we assume the same for you. For that reason we have created Workflow Automations.

### What are Workflow Automations?

Use Workflow Automations to create all kinds of (business) logic or rules to automate simple or even complex tasks. They will enable you to implement logic so that you can build your desired Lead Generation Workflow. An example is tagging visitors who fulfil specific criteria.

{% hint style="success" %}
A basic Workflow consist of a Trigger (rule) and an Action
{% endhint %}

But Workflows can also contain multiple triggers with multiple Actions if needed.

<figure><img src="../../.gitbook/assets/Screenshot 2023-02-23 at 14.19.27.png" alt=""><figcaption><p>An example list of workflows</p></figcaption></figure>

### Triggers

A trigger is basically 1 or more rule(s) that must be met, in order to 'trigger' the start of an automation.

Example Trigger: If a certain page (URL) is visited.

#### Available Triggers:

* Event URL (pageview, email open, custom event)
* A specific Lead Property value for
  * Industry
  * Employee count range
  * country
* LeadBoard (check for existence and stage)
* Lead Tagged <mark style="color:green;">(coming soon)</mark>
* Owner assigned <mark style="color:green;">(coming soon)</mark>

### Actions

A action is basically a task or something that needs to happen. There are many 'things' we want or need to automate so the list of actions will grow over time as LeadBoxer adds more integrations and features.

#### Available Actions:

* Set or update a Lead tag
* Create a custom property with a value from the session
* Create, or update (move) a LeadBoard card
* Webhook push <mark style="color:green;">(coming soon)</mark>
* Assign owner <mark style="color:green;">(coming soon)</mark>
* Send Email notification <mark style="color:green;">(coming soon)</mark>

<figure><img src="../../.gitbook/assets/Screenshot 2023-02-23 at 14.18.25.png" alt=""><figcaption></figcaption></figure>

### Real life Examples

The most simple example is to <mark style="background-color:orange;">tag</mark> a web visitor if they visit a certain page:

* Tag a web visitor as <mark style="color:red;background-color:red;">Job-seeker</mark> if they visit the /jobs.html page
* Tag a web visitor as <mark style="color:blue;background-color:blue;">Customer</mark> if they log into your portal or app
* Tag a web visitor as <mark style="color:green;background-color:green;">Prospect</mark> if they download a white-paper

More advanced examples:

* Create a new leadboard card on LeadBoard 'Canada Sales' on stage 'New leads' when identified company has Industry 'Accounting' and company size is 51-200 and country is 'Canada.
* Move LeadBoard card to stage 'engaged' when email 'white-paper' is opened.
* Set custom field 'Conversion campaign' with value from UTM field when a conversion (eg thank-you pageview) happens.



{% content-ref url="../../guides/how-to-create-a-workflow-automation.md" %}
[how-to-create-a-workflow-automation.md](../../guides/how-to-create-a-workflow-automation.md)
{% endcontent-ref %}
