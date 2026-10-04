# Eloqua

In order to use LeadBoxer together with Oracle Eloqua, you need to make some small edits to your templates.&#x20;

To get going you need to:

1. Add the tracking pixel to register the email open events
2. Modify the links (urls) pointing to your site with additional 'Field merges'

**1. Add email tracking pixel**&#x20;

Simply use the [generic tutorial for email tracking](track-email-opens.md) and select Eloqua from the list of vendors.

**2. Track link Clicks and identify persons on your site**

Follow the generic tutorial and use the 'Field merges' as you have defined them in your account.

Example:

```
https://www.leadboxer.com&email=<span class=eloquaemail>EmailAddress</span>
```

Still need help? [Contact us](mailto:hello@leadboxer.com)
