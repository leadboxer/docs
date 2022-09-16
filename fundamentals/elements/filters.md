# Filters

## Narrowing down the results

When you’ve loaded the LeadBoxer Leads view, you can search and filter your leads. Leadboxer Searching and applying filters each have their own characteristics.

### Filtering

Setting up filters allows you to search very specifically. For instance, you can set up a filter that only shows Dutch companies in the consumer electronics industry that have visited your website in the past 48 hours. The different filter operators also allow you to use search operators, like ‘is’, ‘does not contain’, or ‘has any value’. In addition, filters can be saved into Segments; this allows you to instantly apply any pre-set filter to your list of leads.

### Using filters

The Leadboxer filter allows you to apply criteria to your search. There are three components to each criterion: the category, the operator, and the value. You can enable filters in more than 10 different categories, like company name or city. For each category you select an operator and filter. When using filters, simply choose the filters, operators, and terms of your choice and press ‘apply’ (to search instantly) or ‘save’ (to save the filter into a Segment).

### Searching

In order to search through your leads, simply enter a search string in the search bar at the top right corner of the Leadboard. The search function will check all contents of the leads, so not only the company name. For instance, if you type in ‘coffee’ this will result in all company names that contain coffee, like ‘Johnny’s Coffee’. However, if the company’s description contains a sentence like ‘why not drop by for a cup of coffee’, this will also pop up in the search results. This makes the search function very suitable for a quick and specific search, but less suitable for more in-depth searching.

#### Operators

The Leadboxer interface offers multiple filters. For each filter you can set a parameter based on a filter operator (see below).

| Company name | Filter by company name. Tip: select ‘contains any value’ from the operators list, and the filter will only return leads with identified company names!                                                                                                                                                                                                                     |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Country      | Filter by country                                                                                                                                                                                                                                                                                                                                                          |
| Region       | Filter by region                                                                                                                                                                                                                                                                                                                                                           |
| City         | Filter by city                                                                                                                                                                                                                                                                                                                                                             |
| Industry     | Filter by industry. Industry type is based on the LinkedIn industry types. The industry type search field features a drop-down menu so you can easily select the industry you’re looking for. What’s more, you can only select industries that are relevant to your lead list - meaning there aren’t any irrelevant terms to search through to find the industry you need. |
| Company Size | <p>Self-employed1-10 employees11-50 employees</p><p>51-200 employees</p><p>201-500 employees</p><p>501-1000 employees</p><p>1001-5000 employees</p><p>5001-10,000 employees</p><p>10,001+ employees</p>                                                                                                                                                                    |
| UTM Tags     | UTM tags allow you to search for all leads that have been referred to your website by a specific campaign. For instance, this allows you to search all leads that were directed to your website from a Google paid search, Facebook campaign or emailing.                                                                                                                  |
| Visits       | Each time a lead visits your website, this counts as a visit. Leadboxer will count a new visit after at least thirty minutes of absence, so if a visitor leaves and returns within 30 minutes this still counts as one.                                                                                                                                                    |
| Page Views   | Each time a visitor goes to a different page on your website this counts as a page view. If a visitor goes to your website, and visits three pages in total, this counts as one visit with three page views.                                                                                                                                                               |
| Last Seen    | The time and date that a lead has last visited your website.                                                                                                                                                                                                                                                                                                               |

#### Operators

For each filter you can select a filter operator. Not all operators are available for each filter.  Each operator works as follows:

| None             | No filter will be applied                                                                                                                                                                                                                                                    |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Is               | Results will be \[value]. Use this filter if you want to search for an exact value. For instance, if you want to look for all leads from a company called ‘XYZ’, the filter will return values with company name ‘XYZ’ only.                                                 |
| Is not           | Results will not be \[value]. Use this filter if you want to exclude a specific value. For instance, if you want to exclude all leads from Amsterdam, use the filter City > Is not ‘Amsterdam’.                                                                              |
| Contains         | Results will contain \[value]. Use this filter if you want the results to return all leads containing the value. For instance, if you use the filter Company name > Contains ‘lead’, this will return all company names containing ‘lead’, like leadboxer, xlead, or zleady. |
| Does not contain | Results will not contain \[value]. Use this filter if you want to exclude all leads containing this value. This is different from the ‘is not’ operator - ‘is not’ will only exclude exact values whereas ‘does not contain’ excludes all results containing the value.      |
| Is unknown       | Results will only show unknown values. This option can be used if you only want leads from unknown companies ???                                                                                                                                                             |
| Has any value    | Results will only show known values. By using this filter option, results will only return leads with a value for a specific parameter, for instance known company name or known region.                                                                                     |
| Greater than     | Numerical - Filter will return results greater than parameter value. This filter option may be used for instance if you want to search for leads that have visited your website more than 3 times in total.                                                                  |
| Less than        | Numerical - Filter will return results less than parameter value. This filter option may be used for instance if you want to search for leads that have visited your website more than 3 times in total.                                                                     |
| Between          | Numerical - Filter will return results between two parameter values.                                                                                                                                                                                                         |
| Not between      | Numerical - Filter will return all results except those between the two parameter values.                                                                                                                                                                                    |

####

**Automated e-mail notifications**

In the Leadboxer interface, you also have the option to configure automated e-mail updates. You can configure automated e-mail updates separately for each Segment. In order to do so, check this  tutorial:

{% content-ref url="../../guides/how-to-create-a-notification.md" %}
[how-to-create-a-notification.md](../../guides/how-to-create-a-notification.md)
{% endcontent-ref %}
