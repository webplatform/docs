---
title: Forms
attributions:
  - 'Facebook HTML5 Resource Center.'
notes:
  - 'Should be merged into http://docs.webplatform.org/wiki/guides/html5_form_features'
readiness: 'Not Ready'
summary: 'One of HTML5''s many new features is enhancements to forms. This includes new types of inputs (email, phone number, etc), attributes (form validation and styling), and elements (progress bar, meter, output, etc). Since these features are relatively new, support across browsers can vary. You should keep this in mind as you develop your web app to make it the best possible user experience across all browsers. In this document we will discuss the new features, how to detect and handle non-supporting browsers, and mobile considerations.'
tags:
  - Tutorials
  - JavaScript
uri: tutorials/forms

---
## <span>Summary</span>

One of HTML5's many new features is enhancements to forms. This includes new types of inputs (email, phone number, etc), attributes (form validation and styling), and elements (progress bar, meter, output, etc). Since these features are relatively new, support across browsers can vary. You should keep this in mind as you develop your web app to make it the best possible user experience across all browsers. In this document we will discuss the new features, how to detect and handle non-supporting browsers, and mobile considerations.

## <span>Input Types</span>

HTML5 has expanded the types that are supported by the form input element. For example, here's a simple text input.

    <input type="text" value="my value" />

There were other input types, for example the `password` type. With these types, and especially the text type, developers have created web forms to represent things like emails, web links, and date fields. As a developer, you probably also added client-side field validation to make sure an email entered was valid or that the user entered all the required fields for your form. You may also have created specialized user interfaces for certain input types such as a date picker.

With the introduction of HTML5, your life as a web developer has just become much easier. HTML5 introduces input types to represent the most popular types, which means you can get the supporting browsers to take care of the formatting and handle the input validation.

Switching to a new input type such as the `email` type will not break on browsers that do not support them. Every browser that does not recognize your input type will default to representing it as type `text`. This allows you to make the immediate switch to the new HTML input types, confident that older browser should still work as expected.

See the compatibility section below for more details on how to handle browsers that do not support the new input types.

The new types introduced include:

### <span>Email</span>

Previously, to handle an email input field you would use a `text` type and write JavaScript to validate the input field upon user submission. Now you simply specify an `email` type and let supporting browsers take care of specialized displays and validation. For example, on the iPhone's Safari browser, it will specially handle the `email` type by displaying a custom keyboard with characters related to email input. See an [example of this field in action](http://wufoo.com/html5/types/1-email.html).

### <span>Number</span>

The number input type displays a spinbox control that allows the user to increment and decrement whole numbers. Supporting browsers take care of specialized displays and validation. For example, Chrome will not allow you to type in an invalid field. The iPhone Safari browser will show a number-based keyboard. This input type has optional `min`, `max`, and `step` attributes to help specify acceptable values and ranges. See an [example of this field in action](http://wufoo.com/html5/types/7-number.html).

### <span>Range</span>

Unlike the number input type, range can be fractional and is typically displayed as a slider control. This input type has optional `min`, `max`, and `step` attributes to help specify acceptable values and ranges. See an [example of this field in action](http://wufoo.com/html5/types/8-range.html).

### <span>URL</span>

Most supporting browsers will validate the URL field upon form submission. Browsers will render this field as a normal text entry field. The iPhone Safari browser will render a specialized keyboard for entering URL fields. See an [example of this field in action](http://wufoo.com/html5/types/3-url.html).

### <span>Date Picker</span>

There is a collection of inputs that allow you to implement a date picker. Previously you would have to script these yourself. The six defined input types for selecting a date are `date`, `month`, `week`, `time`, `datetime`, and `datetime-local`. Supporting browsers will implement these types through specialized displays. For example, the Opera browser displays the `date` field by showing a calendar representing a date. See an [example of this field in action](http://wufoo.com/html5/types/4-date.html).

### <span>Telephone Number</span>

To validate the user input you should specify a `pattern` attribute. Browsers will render this field as a normal text entry field. The iPhone Safari browser will render a specialized keyboard for entering telephone fields. See an [example of this field in action](http://wufoo.com/html5/types/2-tel.html).

### <span>Search</span>

Supporting browsers may display this field in a special way for example showing an x button so the user can easily clear the search input. See an [example of this field in action](http://wufoo.com/html5/types/5-search.html).

### <span>Color</span>

This allows you to pick a color. It returns the RGB hexadecimal value of the chosen color. See an [example of this field in action](http://wufoo.com/html5/types/6-color.html).

## <span>Form Attributes</span>

HTML5 has introduced additional attributes to form inputs and elements. These attributes enable functionality including form validation, showing placeholder input text, controlling cursor focus, required form fields, regular expressions for field validation, and others. [Wufoo's Current State of HTML5 Forms](http://wufoo.com/html5/#attributes) lists all of the new form attributes.

See the compatibility section of this doc, below, for more details on how to handle browsers that do not support the new form attributes.

### <span>Form validation</span>

The `required` attribute can be added to any form element that must be filled out before a form is submitted. The browser will then look at the form element type and validate the entry before submitting the form. Here's an example.

    <input type="text" required>

This will tell the browser to check for a non-empty value before form submission. The browsers will also display an appropriate error message. You can override and customize the error message displayed through JavaScript by calling the `setCustomValidity()` method for a form element.

    var myInput = document.getElementById("myInput");
    myInput.setCustomValidity("My custom error message");

You can also turn off validation on a form by setting the `novalidate` attribute for a form.

    <form novalidate>
      <input type="email" value="">
      <input type="submit" value="Send">
    </form>

The form element validation and error message is dependent on the input type as well as a `pattern` attribute if it is defined. For example, if the element is an `email` input type then the browser will check if it is a valid, non-empty value and display a relevant message related to email validation. The `pattern` attribute can be used to specify a custom regular expression (regex) for validation. Here's an example.

    <input type="text" name="username" pattern="^[a-zA-Z][a-zA-Z0-9]{1,10}$">

This specifies a pattern check for a username field of type `text` that should be 2-10 characters, starting with a letter and otherwise alphanumeric. You can find a list of [useful HTML5 patterns here](http://html5pattern.com/). If you wish to check for a non-empty value then be sure to add the `required` attribute, as well.

In addition to the validation methods discussed thus far, there is a constraints validation API that provides a built in methods, attributes, and events that can help you with form validation. For example, each form element has a `validity` attribute that returns a `ValidityState` object describing the validity state that the element is in. You can use this API to do your own validity checks or perform styling on form elements in a certain state.

Note that even with client-side validation it is very important that you also have server-side validation to protect against malicious users who can bypass client-side checks. Client-side validation allows you to offer instant feedback to the user, as it avoids a round trip delay to the server for form validation.

For additional reading, read the form validation [tutorial on A List Apart](http://www.alistapart.com/articles/forward-thinking-form-validation/).

### <span>CSS pseudo classes</span>

HTML5 also introduced CSS pseudo classes. These can be used to control the display of forms elements in certain states or that have certain attributes. For example, you can use CSS to display all required fields with a certain style.

    input:required { background:yellow }

This will show all required input forms with a yellow background. You can also use CSS to display form elements having a certain state.

    input:required:valid { background-color: white }

This will display a white background for all required input forms that have a valid input. The classes that can be used to select form element states include `required`, `optional`, `valid`, `invalid`, `default`, `in-range`, `out-of-range`, `read-only`, and `read-write`. As with other form checks not all pseudo classes are supported in all browsers.

## <span>Form Elements</span>

### <span>Datalist</span>

The `datalist` element is used in conjunction with an input `list` attribute to give the user suggested values. The user can also still enter their own value.

    <input type="text" id="colorChoice" list="myDatalist">
    <datalist id="myDatalist">
      <option label="Red" value="red">
      <option label="Blue" value="blue">
      <option label="Green" value="green">
    </datalist>

### <span>Output</span>

The `output` element which is used to display a result from multiple form fields, such as the addition of two numbers in a form.

    <form id="output_form"
     onsubmit="return false"
     oninput="
      document.getElementById('o').innerHTML =
       parseFloat(document.getElementById('a').value) +
       parseFloat(document.getElementById('b').value)
     "
    >
     <input name="a" id="a" type="number" value="0">
     +
     <input name="b" id="b" type="number" value="0">
     =
     <output name="o" id="o"></output>
    </form>

### <span>Progress</span>

The `progress` element that represents a progress bar. The progress visually flows from 0% to 100% and thus has `max` and `value` attributes. For certain browsers (e.g. Chrome 10+) if the window is not in focus the progress bar will look desaturated.

    <progress max=100 value=50>50%</progress>

### <span>Meter</span>

You can use the `meter` element to represent a measurement. It is visually similar to the `progress` element, but is used for a different purpose- for example, to show the results of a math quiz.

    <meter min=10 max=100 value=65>65%</meter>

### <span>Keygen</span>

The `keygen` element can be used to generate a public key / private key pair.

    <keygen name=key>

## <span>Browser Compatibility</span>

Not all browsers support the new web form features. In order to ensure a good user experience across all browsers, there are several things you can do.

## <span>Feature Detection</span>

Browsers that do not recognize the new input types will fall back to treating them as `text` types. Browsers that do not recognize the new form elements will simply not display them. Your approach for handling this and providing a good user experience should be to first detect support then make use of fallback JavaScript.

### <span>Input Types</span>

One thing to remember for handling older browser is you do not want to throw away any of your existing client-side validation. You can take the following approach to provide fallback support:

1.  Create a dummy or hidden input element.
2.  Set the type attribute to the value you wish to check.
3.  If the browser supports this type it will be retained, otherwise it will contain the type will be `text`.
4.  Check for `text` type to verify your attribute type is supported.

For example,

    function checkInputType(typeToCheck) {
      var myInput = document.createElement("input");
      myInput.setAttribute("type", typeToCheck);
      return myInput.type !== "text";
    }
    // Example, check for "date" type
    if (!checkInputType("date") {
     // Browser does not support type, create
     // fallback HTML
    }

Instead of your creating your own JavaScript functions, there are existing libraries such as [Modernizr](http://www.modernizr.com/). It can be optionally configured to use [various polyfills](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-browser-Polyfills). A polyfill is code that provides fallback support to older browser for a new API or feature that the browser does not natively support.

### <span>Form Attributes</span>

To ensure compatibility with non-supporting browsers you should always have a fallback for your attributes. This depends on the attribute you are using. For example, the `autofocus` attribute allows you to focus an input field without using JavaScript. The fallback would be to use the JavaScript `focus()` method on the input element. Here's an example approach.

1.  Create a dummy or hidden form element
2.  Check that the attribute you are looking for exists in that created element.

For example,

    function checkAttributeSupport(formElement, formAttribute) {
      return formAttribute in document.createElement(formElement);
    }

    // Example, check for "placeholder" attribute in an "input" form element
    if (!checkAttributeSupport("input", "placeholder")) {
      // Browser does not support the attribute
      // for this element, create fallback HTML
    }

[Modernizr](http://www.modernizr.com/) can also be used to easily check for attribute feature support instead of building your own functions. [Modernizr](http://www.modernizr.com/) can be used with the [yepnope.js](http://yepnopejs.com/) script loader library to conditionally load your fallback libraries, known as polyfills, that comprise your JavaScript fallback libraries. It is integrated into [Modernizr](http://www.modernizr.com/), but you can use it separately, for example, if you are using the jQuery library to load fallback libraries.

## <span>Tutorials</span>

The following sites are great resources on browser compatibility and allow you to test the various features from within your browser.

-   [The Current State of HTML5 Forms](http://wufoo.com/html5/)
-   [Dive into HTML5: Forms](http://diveintohtml5.org/forms.html)
-   [CanIUse.com](http://www.caniuse.com)

## <span>Mobile Considerations</span>

Support for HTML5 web forms on mobile browsers is further behind than on desktop browsers. These resources will give you a good sense of what is supported.

-   [The Current State of HTML5 Forms](http://wufoo.com/html5/)
-   [HTML5 Form Inputs on Mobile](http://www.quirksmode.org/html5/inputs_mobile.html)

You can use the same approaches for form feature detection on the mobile browsers as you do on the desktop. The [Modernizr](http://www.modernizr.com/) JavaScript library has a very small footprint and is ideal for both mobile browser feature detection. Also be sure to look through the [GitHub Polyfill repository](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills) for fallback libraries you can use to support mobile browsers.

You also need to be aware of how the mobile browsers handle the display of the new input types. The iPhone will customize the keyboard for the various types. For example, a numerical keyboard will be displayed for `number` type inputs and a URL-friendly keyboard shown for `url` type inputs.