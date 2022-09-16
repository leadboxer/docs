# Lead card: Complete lead details in one page

### **What is a lead card?**

A lead card is a (responsive) webpage that shows all details for any of your website visitors. It contains all the company and personal data, the leadscore graph, all the other lead properties and the complete clickstream /behaviour of the last 5 visits.

### How can i user the lead card?

You can use the lead card to share or visualise the details of your individual website visitors. You can share a lead card by using the share button or by sending the link directly. You can also use the lead card link and add it to your CRM or any other application or and load it in an iframe to show the latest details.

#### Where can i find the URL of a leadcard?

On your leadboard, Click on any lead. Then

1. open the lead properties and&#x20;
2. click on the open lead card link.

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/597262c62c7d3a73488b4d27/file-8JbbBXcfCC.png)

#### How to dynamically generate a lead card link

A lead card link needs a couple of parameters before it can be rendered:

* userId: This is leadboxer used ID and is necessary to calculate the lead score based on the setting of this user ID
* leadId: The userId of the visitor (this can be retrieved from the cookie, see the [lead tags document](https://docs.leadboxer.com/article/96-lead-tags) for an example to get this ID)
* site: the dataset ID
* timezone (optional)

Example:

[https://app.leadboxer.com/view/leaddetail?userId=1132\&leadId=1500387702082.1625569983\&site=20abf326e7508744f6db1950044a1ac3\&timezone=Europe/Amsterdam](https://app.leadboxer.com/view/leaddetail?userId=1132\&leadId=1500387702082.1625569983\&site=20abf326e7508744f6db1950044a1ac3\&timezone=Europe/Amsterdam)

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on January 23, 2019
