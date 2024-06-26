---
description: >-
  Upload a list of accounts /organizations to verify ABM campaign progress or
  success and get notifications for successful engagements
---

# How to upload a List (ABM)

## Instructions

### **Step 1: preparations**

1. Log into LeadBoxer as admin and go to the List Settings page (from the left menu in the bottom )
2. Download the .CSV sample file
3. Open in a spreadsheet application and add your list into the sheet. There are 2 columns:
   1. **organizationDomain**: Put the domain name of the organization in this row&#x20;
   2. **organizationName**: put the name of the organization in this row
4. 'Save As' and (re)name so the file so that it is clear what the list contains. (eg. Target-accounts-2023.csv)

{% hint style="info" %}
**Note**: We will use both the domain OR the name of the organization to match the identified leads or customers to your list.
{% endhint %}

**Wildcards**

we allow for you to use wildcards in both the organizationDomain and organizationName fields.

**Wildcard examples**

| **apple.\*** in organizationDomain                     | Will match all domains from Apple (eg **apple**.com, **apple**.co.uk, **apple**.nl, etc)                               |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| **Intel\*** in organizationName                        | Will match all organizations that Start with the word intel ( **Intel** Corp, **Intel** Germany, **Intel**ligence inc) |
| <p>* <strong>KLM*</strong> in organizationName<br></p> | Will match anything before and after KLM (royal **KLM**, **KLM** international, etc)                                   |

**Troubleshooting**: if you get an error when uploading your .CSV, make sure there are no additional columns in your CSV file. The formatting is strict.

***

### **Step 2: Upload list**

1. Log into LeadBoxer as admin and go to the List overview page
2. Click the Upload button, a new window will appear
3.  Provide a name for your list, select the .CSV file from step 1 and press Save

    <div align="left">

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/6203c2ac68cd260cc2d394a8/file-6EoYoBqchI.png" alt=""><figcaption></figcaption></figure>

    </div>

Here is a screenshot of how it can look like if you have multiple lists:

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/6203c4ac68cd260cc2d394b1/file-swgaATHlK0.png)



### **Step 3: Apply your lists and save in Segment**

Once the list is uploaded, you can use it using the List Filter on the leads & accounts view.

1.  Find and select the list from in the filters when creating a new Segment.

    <div align="left">

    <figure><img src="https://d33v4339jhl8k0.cloudfront.net/docs/assets/565e1cb7c697915b26a5c214/images/6203c3eb025ca67522c795b7/file-D5R7EfJ7RA.png" alt=""><figcaption></figcaption></figure>

    </div>
2. Apply and see the results.
3. Save as segment and optionally set notification, see the [Segment documentation](../fundamentals/elements/segments.md) on how to do this.
