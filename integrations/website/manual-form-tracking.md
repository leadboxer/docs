# Manual form tracking

#### Using javascript to securely send captured form data to LeadBoxer

The LeadBoxer javascript library can be used to capture forms that are submitted by your audience.

The method is straightforward:

1. Using javascript you add the data to a map
2. You send the map data when a form is submitted&#x20;

#### **Notes:**

* There is no limit on the number of key / value pairs you submit
* You might need to add a small delay if you redirect to a 'thank-you' page right after a form is submitted

### Code example for basic form

See the Pen [ExjwYoY](https://codepen.io/LeadBoxer/pen/ExjwYoY) by Wart Fransen ([@LeadBoxer](https://codepen.io/LeadBoxer)) on [CodePen](https://codepen.io/).

**Note: don't forget to run this function when the form is submitted, for example by setting onclick="sendTextForm()" on the submit button.**

#### Delay

When the form submit redirects or reloads the page, it is necessary to delay the form submission for one or two second (literally), in order to create a small window during which the form data can be sent to our servers.

Here are a few examples, using jQuery and pure javascript.

You can do this by adding the following to the bottom of the sendTextForm function

```javascript
setTimeout(function() {
  document.myform.submit();  // replace myform with the <form> name 
},2000);


// This is an example using jQuery
$(‘form’).submit(function (e) {
  var form = this;
  e.preventDefault();
  setTimeout(function () {
    form.submit();
  }, 1000); // in milliseconds
});


// You can also specify the class or ID if you have multiple forms on your page
setTimeout(function () {
    $(".profile-form").submit();
}, 5000);

// Or if you want to use the fancier ES6 syntax:
setTimeout(() => $(".profile-form").submit(), 5000);
```

Working example

For a working example on how to submit form fields go [here](http://api.leadboxer.com/api/examples/forms/index.html)
