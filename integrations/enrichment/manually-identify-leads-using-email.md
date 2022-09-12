# Manually Identify leads using email

#### How does it work?

LeadBoxer is build on top of a full web analytics platform, meaning we can measure anything happening on your site and add this information to the profile of your lead/ visitor /customer. We have an extensive API and javascript library that can be used to enrich profiles from forms, signups, logins, campaigns, etc.

This technology can now also be used to identify individuals from the the personal emails you send out, by passing the lead details using links to your website.

### How can i do this myself?

To identify website visitors from manual emails you send out, you need to:

1. Add one or more links in your email, that link to pages that have the leadBoxer pixel installed.
2. Append the links with tracking parameters of you choice.

LeadBoxer auto captures lead values from these url parameters:

* email
* firstName
* lastName
* companyName
* phoneNumber
* lb\_id

This means that if your visitors views a page with the below URL, we will automatically add these values (email, first name, lastname, etc) to the specific lead.

```
http://www.website.com/?email=jane.doe@company.com&firstName=Jane&lastName=Doe&companyName=ABC&phoneNumber=123
```

### Example

#### Apple Mail

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/595608710428637ff8d43247/file-RdfHwIKiYV.png)

#### lb\_id

The  lb\_id parameter is special. Use this to add your own ID to a visitor so that you can match the visitor to another source. For example a client ID from a online purchase,  a custom build mailing tool or if you cannot use UTM tags

### UTM tags

In case you missed it, we also automatically capture the values for the Google Analytics Tracking parameters aka UTM tags.

* utm\_source
* utm\_medium
* utm\_campaign
* utm\_term
* utm\_content

You can learn about UTM tags in this article:  [Google Analytics Tracking parameters](https://docs.leadboxer.com/article/10-google-analytics)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on October 30, 2019
