# Linkedin InMail or Invite Link Tracking

In this document, we provide an overview or Best Practices on how to track link clicks within your InMail or automated invite campaigns. This will (also) allow you to identify leads who click through to your site, so that you can see what articles and content interest them. This is a type of qualifying behavior we use to identify Buyer Intent.

The problem to overcome is that LinkedIn does not allow you to (visually) link a piece of text, meaning the full URL will be visible in the InMail or Invite.

The goal is to track the links.  Obviously however, your leads are less likely to click a link if they see you are tracking them. So we developed 2 options for a workaround:

1. Add an innocent looking parameter to the url and identify the person on the site manually after they clicked.
2. Use a URL shortener such as bit.ly to mask the full URL and tracking parameters (this will not work for automated campaigns)

#### 1. Manual identification using a URL parameter

In most cases, this is the best option. \
Let's assume you have a list of the high-value target contacts that you are going to automatically send invites or InMails to, and you have selected a tool that can customize the message with custom variables.

Here are the steps:

1. Modify your list of recipients you want to contact via InMail or invite and add a column with an ID.\
   This ID can be anything, in this example we simply choose to use a number.![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5f58a87fc9e77c00160375ee/file-jBZizQYFOw.png)
2. Upload the list to the automation tool you have chosen and make sure the ID is added as a custom field in your audience list
3.  Compose your InMail or Invite message, add your website link and append the link with a parameter that includes the ID.

    **Example:**\
    [https://www.leadboxer.com?ref=23](https://www.leadboxer.com/?ref=23)
4. Send out your campaign (ALWAYS good practice to test)
5. next, in LeadBoxer, create (and save) a new Segment by filtering for the leads that visited a URL with this parameter (see screenshot)
6. When leads show up, you can manually update the anonymous lead by adding their name, email, and role, by looking them up in your spreadsheet.
7. **Cool! you can now see who is actually interested and engaging with your invite or InMail and all their subsequent visits and pageviews**
8. If they subsequently return to your site, we will identify them again automatically and build up the leadscore to qualify

**Note:**\
Make sure our tracking pixel is installed on your website or the landing page!

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/5e739e7a2c7d3a7e9ae97563/file-xfYgFf4RjA.png)

***

#### 2. Automatic identification using a link shortener

Another option is to use the automatic identification using the default parameters.

* Compose the links like this:\
  https://www.leadboxer.com?email=bart@leadboxer.com\&firstName=Bart\&lastName=Fransen\&companyName=LeadBoxer
* Use a link shortener to mask the url and paste that in to your mail
* LeadBoxer will automatically pickup the values of these parameters and update the leads
* NOTE: some email systems will then display a message saying something like: Malicious emails can use shortened links, etc.  In other words, recipients will have to click 'Proceed'.

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on September 9, 2020
