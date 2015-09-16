---
title: 'Making forms fabulous with HTML5'
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/forms/html5forms/)'
notes:
  - 'Should be merged into http://docs.webplatform.org/wiki/guides/html5_form_features'
readiness: 'Not Ready'
summary: 'Improving Web forms through new HTML5 capabilities'
tags:
  - Tutorials
  - HTML
uri: 'tutorials/forms html5forms'

---
**By Jan Kleinert**
Originally published June 2, 2011

## Summary

Improving Web forms through new HTML5 capabilities

## Introduction

Not many people get excited about forms, but HTML5 brings some big improvements, both for the developers creating them and for the users filling them out. New form elements, attributes, input types, browser-based validation, CSS3 styling techniques, and the FormData object make it easier and hopefully more enjoyable to create forms.

### Browser support

At the time of writing, support for all the new form and input elements, attributes and types varies widely across browsers. Even among browsers that support a particular feature, the behavior can be different from one browser to the next. The state of HTML5 forms support is changing very quickly though, and continues to improve. At the time of writing, [these charts](http://wufoo.com/html5/) were the most up-to-date I could find, and they detail the state of browser support for HTML5 forms.

## An overview of what's new

### New elements

HTML5 introduces 5 new elements related to input and forms.

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<thead>
<tr class="header">
<th align="left">Element</th>
<th align="left">Purpose</th>
<th align="left">Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>progress</code></td>
<td align="left">Represents completion of a task.</td>
<td align="left">The <code>progress</code> element could represent the progress of a file being uploaded.</td>
</tr>
<tr class="even">
<td align="left"><code>meter</code></td>
<td align="left">Represents a scalar measurement within a known range.</td>
<td align="left">The <code>meter</code> element could be used to represent something like a temperature or weight measurement.</td>
</tr>
<tr class="odd">
<td align="left"><code>datalist</code></td>
<td align="left">Represents a set of <code>option</code> elements that can be used in
<p>combination with the new <code>list</code> attribute for input to make</p>
dropdown menus.</td>
<td align="left">When the input with the associated datalist gets focus, a dropdown
<p>menu appears and contains the values from the <code>datalist</code>.</p></td>
</tr>
<tr class="even">
<td align="left"><code>keygen</code></td>
<td align="left">A control for key-pair generation.</td>
<td align="left">When the form is submitted, the private key gets stored in the local keystore, and the public key is sent to the server.</td>
</tr>
<tr class="odd">
<td align="left"><code>output</code></td>
<td align="left">Displays the results of a calculation.</td>
<td align="left">An example use of the <code>output</code> element could be to display the sum of the values of two input elements.</td>
</tr>
</tbody>
</table>

### New input types

HTML5 introduces 13 new input types. When viewed in a browser that doesn't support them, these input types fall back to text input.

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<thead>
<tr class="header">
<th align="left">Input Type</th>
<th align="left">Purpose</th>
<th align="left">Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>tel</code></td>
<td align="left">For entering a telephone number.</td>
<td align="left"><code>tel</code> does not enforce a particular syntax, so if you
<p>want to ensure a particular format, you can use <code>pattern</code> or</p>
<code>setCustomValidity()</code> to do additional validation.</td>
</tr>
<tr class="even">
<td align="left"><code>search</code></td>
<td align="left">To prompt users to enter text that they want to search for.</td>
<td align="left">The difference between <code>search</code> and <code>text</code> is
<p>primarily stylistic. Using an input type of <code>search</code> might result in the input field being styled in a way that is consistent with</p>
that platform's search fields.</td>
</tr>
<tr class="odd">
<td align="left"><code>url</code></td>
<td align="left">For entering a single URL.</td>
<td align="left"><code>url</code> is intended for entering a single, <a href="http://www.w3.org/TR/html5/urls.html#absolute-url">absolute URL</a>, which represents a pretty wide range of values.</td>
</tr>
<tr class="even">
<td align="left"><code>email</code></td>
<td align="left">For entering either a single email address or a list of email addresses.</td>
<td align="left">If the <code>multiple</code> attribute is specified, then multiple email addresses can be entered, separated by commas.</td>
</tr>
<tr class="odd">
<td align="left"><code>datetime</code></td>
<td align="left">For entering a date and time with the time zone set to UTC.</td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><code>date</code></td>
<td align="left">For entering a date with no time zone.</td>
<td align="left"></td>
</tr>
<tr class="odd">
<td align="left"><code>month</code></td>
<td align="left">For entering a date with a year and a month, but no time zone.</td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><code>week</code></td>
<td align="left">For entering a date that consists of a week-year number and a week number, but no time zone.</td>
<td align="left">An example of this format is 2011-W05 for the fifth week of 2011.</td>
</tr>
<tr class="odd">
<td align="left"><code>time</code></td>
<td align="left">For entering a time value with hour, minute, seconds, and fractional seconds, but no time zone.</td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><code>datetime-local</code></td>
<td align="left">For entering a date and time with no time zone.</td>
<td align="left"></td>
</tr>
<tr class="odd">
<td align="left"><code>number</code></td>
<td align="left">For numerical input.</td>
<td align="left">Valid values are <a href="http://www.w3.org/TR/html5/common-microsyntaxes.html#valid-floating-point-number">floating point numbers</a>.</td>
</tr>
<tr class="even">
<td align="left"><code>range</code></td>
<td align="left">For numerical input, but unlike <code>number</code>, the actual is not important.</td>
<td align="left">The implementation of the range control is a slider in most browsers that support it.</td>
</tr>
<tr class="odd">
<td align="left"><code>color</code></td>
<td align="left">For choosing color through a color well control.</td>
<td align="left">The value must be a <a href="http://www.w3.org/TR/html5/common-microsyntaxes.html#valid-lowercase-simple-color">valid lowercase simple color</a> such as #ffffff.</td>
</tr>
</tbody>
</table>

### New input attributes

HTML5 also introduces several new attributes for the input and form elements.

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<thead>
<tr class="header">
<th align="left">Attribute</th>
<th align="left">Purpose</th>
<th align="left">Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>autofocus</code></td>
<td align="left">Focuses the input on the element when the page is loaded.</td>
<td align="left"><code>autofocus</code> can be applied to input, select, textarea, and button.</td>
</tr>
<tr class="even">
<td align="left"><code>placeholder</code></td>
<td align="left">Gives the user a hint about what sort of data they should enter.</td>
<td align="left">The placeholder value is displayed in light text
<p>until the element gets focus and the user enters some data. It can be</p>
specified on input and textarea.</td>
</tr>
<tr class="odd">
<td align="left"><code>form</code></td>
<td align="left">Specifies one or more forms to which the input element belongs.</td>
<td align="left">By using the <code>form</code> attribute, the input elements can be
<p>placed anywhere on the page, not just within the form element. Also, a</p>
single input element can be associated with more than one form.</td>
</tr>
<tr class="even">
<td align="left"><code>required</code></td>
<td align="left">A boolean attribute that means the element is required.</td>
<td align="left">The <code>required</code> attribute is helpful for doing browser-based validation without using custom JavaScript.</td>
</tr>
<tr class="odd">
<td align="left"><code>autocomplete</code></td>
<td align="left">For specifying that a field should not autocomplete or be pre-filled by the browser based on a user's past entries.</td>
<td align="left">The <code>autocomplete</code> attribute for fields like a credit
<p>card number or one-time password, which you don't want autocomplete. By default, <code>autocomplete</code> is in the <code>on</code> state, so</p>
if you want to disable it, set it to <code>off</code>.</td>
</tr>
<tr class="even">
<td align="left"><code>pattern</code></td>
<td align="left">For validating an element's value against a regular expression.</td>
<td align="left">When using a <code>pattern</code>, you should also specify a
<p><code>title</code> value to give the user a description of the pattern</p>
that's expected.</td>
</tr>
<tr class="odd">
<td align="left"><code>dirname</code></td>
<td align="left">For submitting the directionality of the control with the form.</td>
<td align="left">For example, if the user entered text data with right-to-left
<p>directionality and the input element contained the <code>dirname</code> attribute, then an indication of the right-to-left directionality would</p>
be submitted along with the input value.</td>
</tr>
<tr class="even">
<td align="left"><code>novalidate</code></td>
<td align="left">For disabling form submission validation when specified on a form element.</td>
<td align="left"></td>
</tr>
<tr class="odd">
<td align="left"><code>formaction</code></td>
<td align="left">For overriding the action attribute on the form element.</td>
<td align="left">This attribute is supported on <code>input</code> and <code>button</code> elements.</td>
</tr>
<tr class="even">
<td align="left"><code>formenctype</code></td>
<td align="left">For overriding the enctype attribute on the form element.</td>
<td align="left">This attribute is supported on <code>input</code> and <code>button</code> elements.</td>
</tr>
<tr class="odd">
<td align="left"><code>formmethod</code></td>
<td align="left">For overriding the method attribute on the form element.</td>
<td align="left">This attribute is supported on <code>input</code> and <code>button</code> elements.</td>
</tr>
<tr class="even">
<td align="left"><code>formnovalidate</code></td>
<td align="left">For overriding the novalidate attribute on the form element.</td>
<td align="left">This attribute is supported on <code>input</code> and <code>button</code> elements.</td>
</tr>
<tr class="odd">
<td align="left"><code>formtarget</code></td>
<td align="left">For overriding the target attribute on the form element.</td>
<td align="left">This attribute is supported on <code>input</code> and <code>button</code> elements.</td>
</tr>
</tbody>
</table>

### The FormData object

One of the enhancements to `XMLHttpRequest` is the introduction of the ` FormData` object. With the `FormData` object, you can create and send a set of key/value pairs and, optionally, files using `XMLHttpRequest`. When using this technique, the data is sent in the same format as if you'd submitted it via the form's `submit()` method with the encoding type of `multipart/form-data`.

`FormData` gives you a way to create HTML forms on-the-fly using JavaScript, and then submit them using `XMLHttpRequest.send()`. Here's a simple example:

    var formData = new FormData();
    formData.append("part_num", "123ABC");
    formData.append("part_price", 7.95);
    formData.append("part_image", somefile)

    var xhr = new XMLHttpRequest();
    xhr.open("POST", "http://some.url/");
    xhr.send(formData);

You can also use `FormData` to add additional data to an existing form before submitting it.

    var formElement = document.getElementById("someFormElement");
    var formData = new FormData(formElement);
    formData.append("part_description", "The best part ever!");

    var xhr = new XMLHttpRequest();
    xhr.open("POST", "http://some.url/");
    xhr.send(formData);

## Browser-based validation

Let's be honest. Validating form data is a pretty boring task, but you need to do it anyway. To do client-side form validation today, you probably write some custom JavaScript code or use a library to do things like check for valid inputs or ensure required fields are filled out before the form is submitted.

New input attributes like `required` and `pattern` used in combination with CSS pseudo-class selectors make it easier to write the checks and display feedback to the user. There are other advanced validation techniques that allow you to use JavaScript to set custom validity rules and messages or to determine if an element is invalid and the reason why.

### The required attribute

If the `required` attribute is present, then the field must contain a value when the form is submitted. Here's an example of an input field for a required email address that ensures that the field has a value and that the value is a valid email address, as defined [here](http://dev.w3.org/html5/spec/Overview.html#valid-e-mail-address).

    <input type="email" id="email_addr" name="email_addr" required />

### The pattern attribute

The `pattern` attribute specified a regular expression used to validate an input field. This example represents a required text input field for a part number. For the purpose of the example, let's say a part number consists of three uppercase letters followed by four digits. The use of `required` and `pattern` ensure that the field has a value and that the value matches the correct format for a part number. If the user hovers over the field, the message in the title attribute is displayed.

    <input type="text" id="part" name="part" required pattern="[A-Z]{3}[0-9]{4}"
           title="Part numbers consist of 3 uppercase letters followed by 4 digits."/>

Building on the previous example, you can also outline the input field in red if an invalid part number is entered. To do that, add this CSS to put a red border around the input field if the value is invalid.

    :invalid {
       border: 2px solid #ff0000;
     }

### The formnovalidate attribute

The `formnovalidate` attribute can be applied to `input` or `button` elements. If it's present, then form submission validation is disabled. Here's an example where submitting a form via the Submit button requires valid input, but submitting via the Save button does not.

    <input type="text" id="part" name="part" required pattern="[A-Z]{3}[0-9]{4}"
           title="Part numbers consist of 3 uppercase letters followed by 4 digits."/>
    <input type="submit" formnovalidate value="Save">
    <input type="submit" value="Submit">

### The constraint validation API

The [constraint validation API](http://dev.w3.org/html5/spec/association-of-controls-and-forms.html#the-constraint-validation-api) gives you powerful tools for handling custom validation. The API allows you to do things like set a custom error, check whether an element is valid, and determine the reason that an element is invalid. Here's an example that displays a custom error if the values in two fields do not match.

    <label>Email:</label>
     <input type="email" id="email_addr" name="email_addr">

     <label>Repeat Email Address:</label>
     <input type="email" id="email_addr_repeat" name="email_addr_repeat" oninput="check(this)">

     <script>
     function check(input) {
       if (input.value != document.getElementById('email_addr').value) {
         input.setCustomValidity('The two email addresses must match.');
       } else {
         // input is valid -- reset the error message
         input.setCustomValidity('');
       }
     }
     </script>

## Putting it all together

Here's an example for a reservation request form that pulls together different input types, form validation, and CSS selectors and styling.

This is the HTML and JavaScript for the form:

    <form oninput="total.value = (nights.valueAsNumber * 99) +
      ((guests.valueAsNumber - 1) * 10)">

       <label>Full name:</label>
       <input type="text" id="full_name" name="full_name" placeholder="Jane Doe" required>

       <label>Email address:</label>
       <input type="email" id="email_addr" name="email_addr" required>

       <label>Repeat email address:</label>
       <input type="email" id="email_addr_repeat" name="email_addr_repeat" required
        oninput="check(this)">

       <label>Arrival date:</label>
       <input type="date" id="arrival_dt" name="arrival_dt" required>

       <label>Number of nights (rooms are $99.00 per night):</label>
       <input type="number" id="nights" name="nights" value="1" min="1" max="30" required>

       <label>Number of guests (each additional guest adds $10.00 per night):</label>
       <input type="number" id="guests" name="guests" value="1" min="1" max="4" required>

       <label>Estimated total:</label>
       $<output id="total" name="total">99</output>.00
       <br><br>

       <label>Promo code:</label>
       <input type="text" id="promo" name="promo" pattern="[A-Za-z0-9]{6}"
        title="Promo codes consist of 6 alphanumeric characters.">

       <input type="submit" value="Request Reservation" />
     </form>

     <script>
     function check(input) {
       if (input.value != document.getElementById('email_addr').value) {
         input.setCustomValidity('The two email addresses must match.');
       } else {
         // input is valid -- reset the error message
         input.setCustomValidity('');
       }
     }
     </script>


This is the CSS that goes with the form code:

    :invalid {
       border-color: #e88;
       -webkit-box-shadow: 0 0 5px rgba(255, 0, 0, .8);
       -moz-box-shadow: 0 0 5px rbba(255, 0, 0, .8);
       -o-box-shadow: 0 0 5px rbba(255, 0, 0, .8);
       -ms-box-shadow: 0 0 5px rbba(255, 0, 0, .8);
       box-shadow:0 0 5px rgba(255, 0, 0, .8);
     }

     :required {
       border-color: #88a;
       -webkit-box-shadow: 0 0 5px rgba(0, 0, 255, .5);
       -moz-box-shadow: 0 0 5px rgba(0, 0, 255, .5);
       -o-box-shadow: 0 0 5px rgba(0, 0, 255, .5);
       -ms-box-shadow: 0 0 5px rgba(0, 0, 255, .5);
       box-shadow: 0 0 5px rgba(0, 0, 255, .5);
     }

     form {
       width:300px;
       margin: 20px auto;
     }

     input {
       font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
       border:1px solid #ccc;
       font-size:20px;
       width:300px;
       min-height:30px;
       display:block;
       margin-bottom:15px;
       margin-top:5px;
       outline: none;

       -webkit-border-radius:5px;
       -moz-border-radius:5px;
       -o-border-radius:5px;
       -ms-border-radius:5px;
       border-radius:5px;
     }

     input[type=submit] {
       background:none;
       padding:10px;
     }

## Resources

-   [W3C Specification](http://www.w3.org/TR/html5/forms.html)
-   [The Current State of HTML5 Forms](http://wufoo.com/html5/)
