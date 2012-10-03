{{Page_Title|Making forms fabulous with HTML5}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Jan Kleinert
|Published=June 2, 2011
}}
{{Summary_Section|Improving Web forms through new HTML5 capabilities}}
{{Tutorial
|Content===Introduction==

Not many people get excited about forms, but HTML5 brings some big improvements, both for the developers creating them and for the users filling them out. New form elements, attributes, input types, browser-based validation, CSS3 styling techniques, and the FormData object make it easier and hopefully more enjoyable to create forms.

===Browser support===

At the time of writing, support for all the new form and input elements, attributes and types varies widely across browsers. Even among browsers that support a particular feature, the behavior can be different from one browser to the next. The state of HTML5 forms support is changing very quickly though, and continues to improve. At the time of writing, [http://wufoo.com/html5/ these charts] were the most up-to-date I could find, and they detail the state of browser support for HTML5 forms.

==An overview of what's new==

===New elements===

HTML5 introduces 5 new elements related to input and forms.

<table class="alternating">
<tr>
<th>Element</th>
<th>Purpose</th>
<th>Notes</th>
</tr>
<tr>
<td><code>[http://dev.w3.org/html5/spec/Overview.html#the-progress-element progress]</code></td>
<td>Represents completion of a task.</td>
<td>The <code>progress</code> element could represent the progress of a
file being uploaded.</td>
</tr>
<tr>
<td><code>[http://dev.w3.org/html5/spec/Overview.html#the-meter-element meter]</code></td>
<td>Represents a scalar measurement within a known range.</td>
<td>The <code>meter</code> element could be used to represent something
like a temperature or weight measurement.</td>
</tr>
<tr>
<td><code>[http://dev.w3.org/html5/spec/Overview.html#the-datalist-element datalist]</code></td>
<td>Represents a set of <code>option</code> elements that can be used in
combination with the new <code>list</code> attribute for input to make
dropdown menus.</td>
<td>When the input with the associated datalist gets focus, a dropdown
menu appears and contains the values from the <code>datalist</code>.
</td>
</tr>
<tr>
<td><code>[http://dev.w3.org/html5/spec/Overview.html#the-keygen-element keygen]</code></td>
<td>A control for key-pair generation.</td>
<td>When the form is submitted, the private key gets stored in the local
keystore, and the public key is sent to the server.</td>
</tr>
<tr>
<td><code>[http://dev.w3.org/html5/spec/Overview.html#the-output-element output]</code></td>
<td>Displays the results of a calculation.</td>
<td>An example use of the <code>output</code> element could be to
display the sum of the values of two input elements.</td>
</tr>
</table>

===New input types===

HTML5 introduces 13 new input types. When viewed in a browser that doesn't support them, these input types fall back to text input.

<table class="alternating">
<tr>
<th>Input Type</th>
<th>Purpose</th>
<th>Notes</th>
</tr>
<tr>
<td><code>tel</code></td>
<td>For entering a telephone number.</td>
<td><code>tel</code> does not enforce a particular syntax, so if you
want to ensure a particular format, you can use <code>pattern</code> or
<code>setCustomValidity()</code> to do additional validation.</td>
</tr>
<tr>
<td><code>search</code></td>
<td>To prompt users to enter text that they want to search for.</td>
<td>The difference between <code>search</code> and <code>text</code> is
primarily stylistic. Using an input type of <code>search</code> might
result in the input field being styled in a way that is consistent with
that platform's search fields.</td>
</tr>
<tr>
<td><code>url</code></td>
<td>For entering a single URL.</td>
<td><code>url</code> is intended for entering a single, [http://www.w3.org/TR/html5/urls.html#absolute-url absolute URL], which represents a pretty wide range of values.</td>
</tr>
<tr>
<td><code>email</code></td>
<td>For entering either a single email address or a list of email
addresses.</td>
<td>If the <code>multiple</code> attribute is specified, then multiple
email addresses can be entered, separated by commas.</td>
</tr>
<tr>
<td><code>datetime</code></td>
<td>For entering a date and time with the time zone set to UTC.</td>
<td></td>
</tr>
<tr>
<td><code>date</code></td>
<td>For entering a date with no time zone.</td>
<td></td>
</tr>
<tr>
<td><code>month</code></td>
<td>For entering a date with a year and a month, but no time zone.</td>
<td></td>
</tr>
<tr>
<td><code>week</code></td>
<td>For entering a date that consists of a week-year number and a week
number, but no time zone.</td>
<td>An example of this format is 2011-W05 for the fifth week of 2011.
</td>
</tr>
<tr>
<td><code>time</code></td>
<td>For entering a time value with hour, minute, seconds, and fractional
seconds, but no time zone.</td>
<td></td>
</tr>
<tr>
<td><code>datetime-local</code></td>
<td>For entering a date and time with no time zone.</td>
<td></td>
</tr>
<tr>
<td><code>number</code></td>
<td>For numerical input.</td>
<td>Valid values are [http://www.w3.org/TR/html5/common-microsyntaxes.html#valid-floating-point-number floating point numbers].</td>
</tr>
<tr>
<td><code>range</code></td>
<td>For numerical input, but unlike <code>number</code>, the actual
is not important.</td>
<td>The implementation of the range control is a slider in most
browsers that support it.</td>
</tr>
<tr>
<td><code>color</code></td>
<td>For choosing color through a color well control.</td>
<td>The value must be a
[http://www.w3.org/TR/html5/common-microsyntaxes.html#valid-lowercase-simple-color valid lowercase simple color] such as #ffffff.</td>
</tr>
</table>

===New input attributes===

HTML5 also introduces several new attributes for the input and form elements.

<table class="alternating">
<tr>
<th scope="col">Attribute</th>
<th scope="col">Purpose</th>
<th scope="col">Notes</th>
</tr>
<tr>
<td><code>autofocus</code></td>
<td>Focuses the input on the element when the page is loaded.</td>
<td><code>autofocus</code> can be applied to input, select, textarea,
and button.</td>
</tr>
<tr>
<td><code>placeholder</code></td>
<td>Gives the user a hint about what sort of data they should enter.</td>
<td>The placeholder value is displayed in light text
until the element gets focus and the user enters some data. It can be
specified on input and textarea.</td>
</tr>
<tr>
<td><code>form</code></td>
<td>Specifies one or more forms to which the input element belongs.</td>
<td>By using the <code>form</code> attribute, the input elements can be
placed anywhere on the page, not just within the form element. Also, a
single input element can be associated with more than one form.</td>
</tr>
<tr>
<td><code>required</code></td>
<td>A boolean attribute that means the element is required.</td>
<td>The <code>required</code> attribute is helpful for doing
browser-based validation without using custom JavaScript.</td>
</tr>
<tr>
<td><code>autocomplete</code></td>
<td>For specifying that a field should not autocomplete or be pre-filled
by the browser based on a user's past entries.</td>
<td>The <code>autocomplete</code> attribute for fields like a credit
card number or one-time password, which you don't want autocomplete. By
default, <code>autocomplete</code> is in the <code>on</code> state, so
if you want to disable it, set it to <code>off</code>.</td>
</tr>
<tr>
<td><code>pattern</code></td>
<td>For validating an element's value against a regular expression.</td>
<td>When using a <code>pattern</code>, you should also specify a
<code>title</code> value to give the user a description of the pattern
that's expected.</td>
</tr>
<tr>
<td><code>dirname</code></td>
<td>For submitting the directionality of the control with the form.</td>
<td>For example, if the user entered text data with right-to-left
directionality and the input element contained the <code>dirname</code>
attribute, then an indication of the right-to-left directionality would
be submitted along with the input value.</td>
</tr>
<tr>
<td><code>novalidate</code></td>
<td>For disabling form submission validation when specified on a form
element.</td>
<td></td>
</tr>
<tr>
<td><code>formaction</code></td>
<td>For overriding the action attribute on the form element.</td>
<td>This attribute is supported on <code>input</code> and
<code>button</code> elements.</td>
</tr>
<tr>
<td><code>formenctype</code></td>
<td>For overriding the enctype attribute on the form element.</td>
<td>This attribute is supported on <code>input</code> and
<code>button</code> elements.</td>
</tr>
<tr>
<td><code>formmethod</code></td>
<td>For overriding the method attribute on the form element.</td>
<td>This attribute is supported on <code>input</code> and
<code>button</code> elements.</td>
</tr>
<tr>
<td><code>formnovalidate</code></td>
<td>For overriding the novalidate attribute on the form element.</td>
<td>This attribute is supported on <code>input</code> and
<code>button</code> elements.</td>
</tr>
<tr>
<td><code>formtarget</code></td>
<td>For overriding the target attribute on the form element.</td>
<td>This attribute is supported on <code>input</code> and
<code>button</code> elements.</td>
</tr>
</table>

===The FormData object===

One of the enhancements to <code>[http://dev.w3.org/2006/webapi/XMLHttpRequest-2 XMLHttpRequest]</code> is the introduction of the <code> [http://dev.w3.org/2006/webapi/XMLHttpRequest-2/#the-formdata-interface FormData]</code> object. With the <code>FormData</code> object, you can create and send a set of key/value pairs and, optionally, files using <code>XMLHttpRequest</code>. When using this technique, the data is sent in the same format as if you'd submitted it via the form's <code>submit()</code> method with the encoding type of <code>multipart/form-data</code>.

<code>FormData</code> gives you a way to create HTML forms on-the-fly using JavaScript, and then submit them using <code>XMLHttpRequest.send()</code>. Here's a simple example:

 var formData = new FormData();
 formData.append("part_num", "123ABC");
 formData.append("part_price", 7.95);
 formData.append("part_image", somefile)
 
 var xhr = new XMLHttpRequest();
 xhr.open("POST", "http://some.url/");
 xhr.send(formData);

You can also use <code>FormData</code> to add additional data to an existing form before submitting it.

 var formElement = document.getElementById("someFormElement");
 var formData = new FormData(formElement);
 formData.append("part_description", "The best part ever!");
 
 var xhr = new XMLHttpRequest();
 xhr.open("POST", "http://some.url/");
 xhr.send(formData);

==Browser-based validation==

Let's be honest. Validating form data is a pretty boring task, but you need to do it anyway. To do client-side form validation today, you probably write some custom JavaScript code or use a library to do things like check for valid inputs or ensure required fields are filled out before the form is submitted.

New input attributes like <code>required</code> and <code>pattern</code> used in combination with CSS pseudo-class selectors make it easier to write the checks and display feedback to the user. There are other advanced validation techniques that allow you to use JavaScript to set custom validity rules and messages or to determine if an element is invalid and the reason why.

===The required attribute===

If the <code>required</code> attribute is present, then the field must contain a value when the form is submitted. Here's an example of an input field for a required email address that ensures that the field has a value and that the value is a valid email address, as defined [http://dev.w3.org/html5/spec/Overview.html#valid-e-mail-address here].<br />

 <input type="email" id="email_addr" name="email_addr" required />

===The pattern attribute===

The <code>pattern</code> attribute specified a regular expression used to validate an input field. This example represents a required text input field for a part number. For the purpose of the example, let's say a part number consists of three uppercase letters followed by four digits. The use of <code>required</code> and <code>pattern</code> ensure that the field has a value and that the value matches the correct format for a part number. If the user hovers over the field, the message in the title attribute is displayed. <br />

 <input type="text" id="part" name="part" required pattern="[A-Z]{3}[0-9]{4}"
        title="Part numbers consist of 3 uppercase letters followed by 4 digits."/>

Building on the previous example, you can also outline the input field in red if an invalid part number is entered. To do that, add this CSS to put a red border around the input field if the value is invalid. <br />

 <nowiki>:invalid {
   border: 2px solid #ff0000;
 }</nowiki>

===The formnovalidate attribute===

The <code>formnovalidate</code> attribute can be applied to <code>input</code> or <code>button</code> elements. If it's present, then form submission validation is disabled. Here's an example where submitting a form via the Submit button requires valid input, but submitting via the Save button does not. <br />

 <input type="text" id="part" name="part" required pattern="[A-Z]{3}[0-9]{4}"
        title="Part numbers consist of 3 uppercase letters followed by 4 digits."/>
 <input type="submit" formnovalidate value="Save">
 <input type="submit" value="Submit">

===The constraint validation API===

The [http://dev.w3.org/html5/spec/association-of-controls-and-forms.html#the-constraint-validation-api constraint validation API] gives you powerful tools for handling custom validation. The API allows you to do things like set a custom error, check whether an element is valid, and determine the reason that an element is invalid. Here's an example that displays a custom error if the values in two fields do not match. <br />

 <nowiki><label>Email:</label>
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
 </script></nowiki>

==Putting it all together==

Here's an example for a reservation request form that pulls together different input types, form validation, and CSS selectors and styling.

This is the HTML and JavaScript for the form:

<nowiki><form oninput="total.value = (nights.valueAsNumber * 99) +
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
 </script></nowiki>

This is the CSS that goes with the form code:

 <nowiki>:invalid {
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
 }</nowiki>

==Resources==

* [http://www.w3.org/TR/html5/forms.html W3C Specification]
* [http://wufoo.com/html5/ The Current State of HTML5 Forms]
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/forms/html5forms/
}}