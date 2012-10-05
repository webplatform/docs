{{Page_Title}}
{{Flags}}
{{Byline}}
{{Summary_Section|One of HTML5's many new features is enhancements to forms. This includes new types of inputs (email, phone number, etc), attributes (form validation and styling), and elements (progress bar, meter, output, etc). Since these features are relatively new, support across browsers can vary. You should keep this in mind as you develop your web app to make it the best possible user experience across all browsers. In this document we will discuss the new features, how to detect and handle non-supporting browsers, and mobile considerations.}}
{{Tutorial
|Content=== Input Types ==

HTML5 has expanded the types that are supported by the form input element. For example, here's a simple text input.

 &lt;input type="text" value="my value" />

There were other input types, for example the <code>password</code> type. With these types, and especially the text type, developers have created web forms to represent things like emails, web links, and date fields. As a developer, you probably also added client-side field validation to make sure an email entered was valid or that the user entered all the required fields for your form. You may also have created specialized user interfaces for certain input types such as a date picker.

With the introduction of HTML5, your life as a web developer has just become much easier. HTML5 introduces input types to represent the most popular types, which means you can get the supporting browsers to take care of the formatting and handle the input validation. 

Switching to a new input type such as the <code>email</code> type will not break on browsers that do not support them. Every browser that does not recognize your input type will default to representing it as type <code>text</code>. This allows you to make the immediate switch to the new HTML input types, confident that older browser should still work as expected. 

See the compatibility section below for more details on how to handle browsers that do not support the new input types.

The new types introduced include:

=== Email ===

Previously, to handle an email input field you would use a <code>text</code> type and write JavaScript to validate the input field upon user submission. Now you simply specify an <code>email</code> type and let supporting browsers take care of specialized displays and validation. For example, on the iPhone's Safari browser, it will specially handle the <code>email</code> type by displaying a custom keyboard with characters related to email input. See an [http://wufoo.com/html5/types/1-email.html example of this field in action].

=== Number ===

The number input type displays a spinbox control that allows the user to increment and decrement whole numbers. Supporting browsers take care of specialized displays and validation. For example, Chrome will not allow you to type in an invalid field. The iPhone Safari browser will show a number-based keyboard. This input type has optional <code>min</code>, <code>max</code>, and <code>step</code> attributes to help specify acceptable values and ranges. See an [http://wufoo.com/html5/types/7-number.html example of this field in action].

=== Range ===

Unlike the number input type, range can be fractional and is typically displayed as a slider control. This input type has optional <code>min</code>, <code>max</code>, and <code>step</code> attributes to help specify acceptable values and ranges. See an [http://wufoo.com/html5/types/8-range.html example of this field in action].

=== URL ===

Most supporting browsers will validate the URL field upon form submission. Browsers will render this field as a normal text entry field. The iPhone Safari browser will render a specialized keyboard for entering URL fields. See an [http://wufoo.com/html5/types/3-url.html example of this field in action].

=== Date Picker ===

There is a collection of inputs that allow you to implement a date picker. Previously you would have to script these yourself. The six defined input types for selecting a date are <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime</code>, and <code>datetime-local</code>. Supporting browsers will implement these types through specialized displays. For example, the Opera browser displays the <code>date</code> field by showing a calendar representing a date. See an [http://wufoo.com/html5/types/4-date.html example of this field in action].

=== Telephone Number ===

To validate the user input you should specify a <code>pattern</code> attribute. Browsers will render this field as a normal text entry field. The iPhone Safari browser will render a specialized keyboard for entering telephone fields. See an [http://wufoo.com/html5/types/2-tel.html example of this field in action].

=== Search ===

Supporting browsers may display this field in a special way for example showing an x button so the user can easily clear the search input. See an [http://wufoo.com/html5/types/5-search.html example of this field in action].

=== Color ===

This allows you to pick a color. It returns the RGB hexadecimal value of the chosen color. See an [http://wufoo.com/html5/types/6-color.html example of this field in action].

== Form Attributes ==

HTML5 has introduced additional attributes to form inputs and elements. These attributes enable functionality including form validation, showing placeholder input text, controlling cursor focus, required form fields, regular expressions for field validation, and others. [http://wufoo.com/html5/#attributes Wufoo's Current State of HTML5 Forms] lists all of the new form attributes.

See the compatibility section of this doc, below, for more details on how to handle browsers that do not support the new form attributes.

=== Form validation ===

The <code>required</code> attribute can be added to any form element that must be filled out before a form is submitted. The browser will then look at the form element type and validate the entry before submitting the form. Here's an example.

 &lt;input type="text" required>

This will tell the browser to check for a non-empty value before form submission. The browsers will also display an appropriate error message. You can override and customize the error message displayed through JavaScript by calling the <code>setCustomValidity()</code> method for a form element.

 var myInput = document.getElementById("myInput");
 myInput.setCustomValidity("My custom error message");

You can also turn off validation on a form by setting the <code>novalidate</code> attribute for a form.

 &lt;form novalidate>
   &lt;input type="email" value="">
   &lt;input type="submit" value="Send">
 &lt;/form>

The form element validation and error message is dependent on the input type as well as a <code>pattern</code> attribute if it is defined. For example, if the element is an <code>email</code> input type then the browser will check if it is a valid, non-empty value and display a relevant message related to email validation. The <code>pattern</code> attribute can be used to specify a custom regular expression (regex) for validation. Here's an example.

 &lt;input type="text" name="username" pattern="^[a-zA-Z][a-zA-Z0-9]{1,10}$">

This specifies a pattern check for a username field of type <code>text</code> that should be 2-10 characters, starting with a letter and otherwise alphanumeric. You can find a list of [http://html5pattern.com/ useful HTML5 patterns here]. If you wish to check for a non-empty value then be sure to add the <code>required</code> attribute, as well.

In addition to the validation methods discussed thus far, there is a constraints validation API that provides a built in methods, attributes, and events that can help you with form validation. For example, each form element has a <code>validity</code> attribute that returns a <code>ValidityState</code> object describing the validity state that the element is in. You can use this API to do your own validity checks or perform styling on form elements in a certain state.

Note that even with client-side validation it is very important that you also have server-side validation to protect against malicious users who can bypass client-side checks. Client-side validation allows you to offer instant feedback to the user, as it avoids a round trip delay to the server for form validation.

For additional reading, read the form validation [http://www.alistapart.com/articles/forward-thinking-form-validation/ tutorial on A List Apart].

=== CSS pseudo classes ===

HTML5 also introduced CSS pseudo classes. These can be used to control the display of forms elements in certain states or that have certain attributes. For example, you can use CSS to display all required fields with a certain style.

 input:required { background:yellow }

This will show all required input forms with a yellow background. You can also use CSS to display form elements having a certain state.

 input:required:valid { background-color: white }

This will display a white background for all required input forms that have a valid input. The classes that can be used to select form element states include <code>required</code>, <code>optional</code>, <code>valid</code>, <code>invalid</code>, <code>default</code>, <code>in-range</code>, <code>out-of-range</code>, <code>read-only</code>, and <code>read-write</code>. As with other form checks not all pseudo classes are supported in all browsers.

== Form Elements ==

=== Datalist ===
The <code>datalist</code> element is used in conjunction with an input <code>list</code> attribute to give the user suggested values. The user can also still enter their own value.

 &lt;input type="text" id="colorChoice" list="myDatalist">
 &lt;datalist id="myDatalist">
   &lt;option label="Red" value="red">
   &lt;option label="Blue" value="blue">
   &lt;option label="Green" value="green">
 &lt;/datalist>

=== Output  ===

The <code>output</code> element which is used to display a result from multiple form fields, such as the addition of two numbers in a form.

 &lt;form id="output_form" 
  onsubmit="return false" 
  oninput="
   document.getElementById('o').innerHTML =
    parseFloat(document.getElementById('a').value) +
    parseFloat(document.getElementById('b').value)
  "
 >
  &lt;input name="a" id="a" type="number" value="0">
  + 
  &lt;input name="b" id="b" type="number" value="0">
  =
  &lt;output name="o" id="o"></output>
 &lt;/form>

=== Progress ===
The <code>progress</code> element that represents a progress bar. The progress visually flows from 0% to 100% and thus has <code>max</code> and <code>value</code> attributes. For certain browsers (e.g. Chrome 10+) if the window is not in focus the progress bar will look desaturated.

 &lt;progress max=100 value=50>50%&lt;/progress>

=== Meter ===
You can use the <code>meter</code> element to represent a measurement. It is visually similar to the <code>progress</code> element, but is used for a different purpose- for example, to show the results of a math quiz.

 &lt;meter min=10 max=100 value=65>65%&lt;/meter>

=== Keygen ===
The <code>keygen</code> element can be used to generate a public key / private key pair.

 &lt;keygen name=key>

== Browser Compatibility ==

Not all browsers support the new web form features. In order to ensure a good user experience across all browsers, there are several things you can do.

== Feature Detection  ==

Browsers that do not recognize the new input types will fall back to treating them as <code>text</code> types. Browsers that do not recognize the new form elements will simply not display them. Your approach for handling this and providing a good user experience should be to first detect support then make use of fallback JavaScript.

=== Input Types ===

One thing to remember for handling older browser is you do not want to throw away any of your existing client-side validation. You can take the following approach to provide fallback support:

1. Create a dummy or hidden input element.
1. Set the type attribute to the value you wish to check.
1. If the browser supports this type it will be retained, otherwise it will contain the type will be <code>text<code>.
1. Check for <code>text</code> type to verify your attribute type is supported.

For example,

 function checkInputType(typeToCheck) {
   var myInput = document.createElement("input");
   myInput.setAttribute("type", typeToCheck);
   return myInput.type !== "text";
 }
 // Example, check for "date" type
 if (!checkInputType("date") {
  // Browser does not support type, create
  // fallback HTML
 }

Instead of your creating your own JavaScript functions, there are existing libraries such as [http://www.modernizr.com/ Modernizr]. It can be optionally configured to use [https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-browser-Polyfills various polyfills]. A polyfill is code that provides fallback support to older browser for a new API or feature that the browser does not natively support.


=== Form Attributes ===

To ensure compatibility with non-supporting browsers you should always have a fallback for your attributes. This depends on the attribute you are using. For example, the <code>autofocus</code> attribute allows you to focus an input field without using JavaScript. The fallback would be to use the JavaScript <code>focus()</code> method on the input element. Here's an example approach.

1. Create a dummy or hidden form element
1. Check that the attribute you are looking for exists in that created element.

For example,

 function checkAttributeSupport(formElement, formAttribute) {
   return formAttribute in document.createElement(formElement);
 }

 // Example, check for "placeholder" attribute in an "input" form element
 if (!checkAttributeSupport("input", "placeholder")) {
   // Browser does not support the attribute
   // for this element, create fallback HTML
 }

[http://www.modernizr.com/ Modernizr] can also be used to easily check for attribute feature support instead of building your own functions. [http://www.modernizr.com/ Modernizr] can be used with the [http://yepnopejs.com/ yepnope.js] script loader library to conditionally load your fallback libraries, known as polyfills, that comprise your JavaScript fallback libraries. It is integrated into [http://www.modernizr.com/ Modernizr], but you can use it separately, for example, if you are using the jQuery library to load fallback libraries.

== Tutorials ==

The following sites are great resources on browser compatibility and allow you to test the various features from within your browser.

* [http://wufoo.com/html5/ The Current State of HTML5 Forms]
* [http://diveintohtml5.org/forms.html Dive into HTML5: Forms]
* [http://www.caniuse.com CanIUse.com]

== Mobile Considerations ==

Support for HTML5 web forms on mobile browsers is further behind than on desktop browsers. These resources will give you a good sense of what is supported.

* [http://wufoo.com/html5/ The Current State of HTML5 Forms]
* [http://www.quirksmode.org/html5/inputs_mobile.html HTML5 Form Inputs on Mobile] 

You can use the same approaches for form feature detection on the mobile browsers as you do on the desktop. The [http://www.modernizr.com/ Modernizr] JavaScript library has a very small footprint and is ideal for both mobile browser feature detection. Also be sure to look through the [https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills GitHub Polyfill repository] for fallback libraries you can use to support mobile browsers.

You also need to be aware of how the mobile browsers handle the display of the new input types. The iPhone will customize the keyboard for the various types. For example, a numerical keyboard will be displayed for <code>number</code> type inputs and a URL-friendly keyboard shown for <code>url</code> type inputs.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=Facebook HTML5 Resource Center
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}