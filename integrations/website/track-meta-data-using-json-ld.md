# Track meta data using JSON-LD

**What is JSON-LD**?&#x20;

When you use [Json-ld](https://json-ld.org/), you are following open standards and schemas, and your metadata is included in a script tag. This metadata can also be used by other services (such as Google, [for enhanced display in search listings](https://developers.google.com/search/docs/guides/intro-structured-data)).

If you would like to capture specific JSON-LD metadata information on your webpages and add these to the profile of your leads or customers, you can do so with the following example

Make sure you read first about how you can [add properties to a lead/customer on page-load](https://docs.leadboxer.com/article/95-advanced-pixel-usage) as we basically build on top of that feature.

#### Example

Here is an example JSON-LD snippet:

```
<script type="application/ld+json">{
    "@context": "https://schema.org",
    "@type": "NewsArticle",
    "url": "https://mysite.com/my-article",
    "creator": "Brad Shaw",
    "keywords": [
        "IFS",
        "Partner Zone",
        "Analytics planning and data analysis",
        "Cloud ERP financials and supply chain",
        "Connected manufacturing",
        "Digital enterprise in the real world",
        "Audio"
    ],
    "headline": "My Headline",
    "name": "My name",
    "description": "desc",
    "datePublished": "2021-06-22T03:35:20-0700",
    "isAccessibleForFree": "True",
    "dateModified": "2021-06-22T03:45:24-0700",
    "articleSection": "ABC"
}</script>
```

Now to capture specific items on page load from above example, you can use javascript to pass this to LeadBoxer. \
We've included some real-life logic in below example for when fields are not populated, empty, not defined, etc.:

```
function ot_onload() {
  // https://stackoverflow.com/questions/38602543/is-there-a-way-to-access-json-ld-via-javascript-if-it-doesnt-have-an-id

  var jsonld = JSON.parse(document.querySelector('script[type="application/ld+json"]').innerText);
  if (typeof jsonld !== 'undefined') {
    var articleSection  = jsonld.articleSection;
    var creator = jsonld.creator; 
    var datePublished;
    if (typeof jsonld.datePublished !== 'undefined')
      datePublished = jsonld.datePublished.substr(0, jsonld.datePublished.indexOf('T'));;

    if (typeof articleSection !== 'undefined') {
//      console.log("got articleSection: " + articleSection); 
      ot_map.put("lb_articleSection", articleSection);
    } else {
//      console.log("got articleSection: undefined");
      ot_map.put("lb_articleSection", "undefined");
    }
    if (typeof creator !== 'undefined') {
//      console.log("got creator: " + creator);
      ot_map.put("lb_creator", creator);
    } else {
      ot_map.put("lb_creator", "undefined");
    }
    if (typeof datePublished !== 'undefined') {
      ot_map.put("lb_datePublished", datePublished);
    } else {
      ot_map.put("lb_datePublished", "undefined");
    }
    ot_map.put("lb_topTitles", document.title + "|" + ot_map.get("lb_datePublished") + "|" + ot_map.get("lb_articleSection") );
//    console.log(ot_map.get("lb_topTitles"));
  }

  // load and log the state of all variables
  ot_log_state();
}
```

Still need help? [Contact Us](broken-reference) [Contact Us](broken-reference)

Last updated on July 7, 2021
