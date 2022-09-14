# Adding client-customer database to LeadBoxer

I want to submit information to LeadBoxer, is this possible?\
For example, I have a database with a list of properties, and I would like to add the information from the database to my LeadBoxer leads.

In other words, can information known about a visitor (lead) to a site tracked by LeadBoxer be sent to LeadBoxer and displayed on the leadboard?&#x20;

The answer is yes, although it’s not possible to send a database to LeadBoxer and have it attached to your list of leads. The way to send data to leadboxer is along with an event that is being measured, for example a login event. Data can be submitted to LeadBoxer in the form of ‘Properties’. The engine is event-based, so you need to send properties when an event is triggered, ie logging in to a site.

When a login-event occurs, you grab all the information from your db that you think is interesting for that login, and send it along to LeadBoxer.

The document tagging leads with properties explains how to do this in technical terms. In other words, how to get things into the leadboard with an event (download or pageview).

Still need help? [Contact Us](broken-reference)

Last updated on September 2, 2022
