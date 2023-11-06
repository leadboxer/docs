# Change website content based on behaviour

_**Q: Can I change the content of my site based on some basic behavioural properties?**_

**A: Yes, this is possible: By reading the LeadBoxer cookies with javascript, you can get basic information like number of sessions and pageviews.**

***

#### LeadBoxer cookies (yum ;)

There are 3 cookies set by the LeadBoxer JavaScript:

1.  **A cookie orientated to keeping user data:**

    ```
    _otui <random number client site>. <first visit start unix timestamp>. <previous visit start unix timestamp>. <current visit start unix timestamp>. <session count>. <life time event view count>
    ```

    **example**

    `_otui 1279273569088.1279273569088.1279273569088.1.13`\

2.  **A cookie orientated to keeping session data:**

    ```
    _ots <session event view count>. <current visit start unix timestamp>. <previous event view unix timestamp>. <current event view unix timestamp
    ```

    **example**

    `_ots 13.1279273569088.1279273785569.1279273833718`
3.  **A cookie orientated to keeping referrer data:**

    ```
    _otr <session first referrer event view unix timestamp>.<referrer url>
    ```

    **example**

    `_otr 1279273431384.http%3A//www.example.com/an/example/referrer.html`

#### Reading a cookie using Javascript

You can read the content of LeadBoxer cookie using javascript, make sure you split the data correctly before processing. See example below.

**Example**

```
<!-- note: you should remove the defer attribute from the script tag to not worry about load on ready stuff -->
<script src="//script.leadboxer.com/?dataset=your dataset id"></script>
<script type="text/javascript">

// get the cookie data and split the numbers
var _otua = _otui.split(".");

// define the values
var sessions = _otua[4];	
var pageviews = _otua[5];	

//alert the session number
alert(sessions);

//alert the user pageview number
alert(pageviews);

</script>
```

Still need help? [Contact Us](broken-reference)

Last updated on May 28, 2019
