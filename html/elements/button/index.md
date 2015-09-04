---
title: button
tags:
  - Markup
  - Elements
  - HTML
  - UI
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
summary: 'The button element represents a clickable button.'
code_samples:
  - 'http://gist.github.com/b08191a8d5915621a5e1'
  - 'http://gist.github.com/ceb6531b1b86fb0b21d0'
  - 'http://gist.github.com/c579515bcd4378bfd634'
uri: html/elements/button

---
# button

## Summary

The button element represents a clickable button.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLButtonElement](/dom/HTMLButtonElement)

You can put text or images inside a button element. If the element is not disabled, the user can activate the button.

By default, the button element is used to submit [**form**](/html/elements/form) data. Modifying the type attribute can change this behavior.

### Attributes (HTML 4)

name
:   The name of the button. This can be used to identify which button was used to submit a form.
type
:   This specifies the type of the button. If omitted, the type is `submit`. The following types are possible:

    -   `submit`: the button submits the form it is associated with and sends the form data to the server. This is the default value.
    -   `reset`: the button resets the form it is associated with. This will set the containing fields to their initial values.
    -   `button`: the button has no default behavior. Useful to bind JavaScript [**click**](/dom/MouseEvent/click) events

value
:   The initial value of the button.
disabled
:   This Boolean attribute indicates that the user cannot interact with the button. If this attribute is not specified, the button inherits its setting from the containing element, for example **fieldset** if there is no containing element with the disabled attribute set, then the button is enabled. A disabled button isn’t clickable.

### Additional attributes (HTML 5, candidate specification)

autofocus
:   When this attribute is set to "true" the button will have input focused after the page loads, unless the user overrides it, for example by typing in a different control. Only one form-associated element in a document can have this attribute specified.
form
:   Specifies which form the button is associated with. The value of the attribute must be the id attribute of the form. If this attribute is not specified, the button must be a descendant of the form itself to be able to submit form data. This attribute enables you to place **button** elements anywhere within a document, not just as descendants of their **form** elements.
formaction
:   The URI of a program that processes the information from the form. When present, it will override the action attribute of the associated form.
formmethod
:   The HTTP method to send the form data. This can either be `post` or `get`. If specified, it will override the method attribute of the associated form. Possible values are:
    -   `post`: The data from the form is included in the body of the form and is sent to the server.
    -   `get`: The data from the form are appended to the form attribute URI, with a '?' as a separator, and the resulting URI is sent to the server. Use this method when the form has no side-effects and contains only ASCII characters.

formnovalidate
:   If the button is a submit button, this attribute specifies whether the form should be validated or not. It overrides the **novalidate** attribute of the form it belongs to.
formtarget
:   This attribute is a keyword, indicating where to display the response that is received after submitting the form. This can be one of the following:

    -   `_self`: load the response into the same context as the form itself. This is the default value.
    -   `_blank`: load the response into a new, unnamed context (Browser window)
    -   `_parent`: loads the response into the parent context. If there is no parent, it will behave the same as \_self.
    -   `_top`: loads the response into the top-most context. This is the browsing context of an ancestor of the current context. If there is no parent, it will behave the same as \_self.

All these attributes, except `name`, have default values and can be omitted.

## Examples

This examples uses the `<button>` element to display a clickable button with out sending or reseting a form.

``` {.html}
<button name="myButton" type="button">Click me</button>
```

[View live example](http://code.webplatform.org/gist/b08191a8d5915621a5e1)

This example shows how to use a submit `<button>` to send a form. Read about the [**form**](/html/elements/form) element to get further information about how to use forms.

``` {.html}
<form action="dataReceiverURI">
  <label for="name">Name:</label>
  <input id="name" type="text" name="user_name">
  <button name="mySubmitButton">Submit</button>
</form>
```

[View live example](http://code.webplatform.org/gist/ceb6531b1b86fb0b21d0)

This example shows how to reset a form with use of `<button="reset">`. Read about the [**form**](/html/elements/form) element to get further information about how to use forms.

``` {.html}
<form>
  <label for="name">Name:</label>
  <input id="name" type="text" name="user_name" >
  <button name="myResetButton">reset</button>
</form>
```

[View live example](http://code.webplatform.org/gist/c579515bcd4378bfd634)

## Usage

     Generally, the button element can be used whenever there should be a button clickable by the user.

The ending tag is mandatory. The button should have a descriptive text inside it, otherwise the button will be empty and the user won't know what the button will do.

Please note that styling a submit button using the \<button\> element is easier than styling an [**input**](/html/elements/input) element with type `submit`.

## Notes

Since the default for the `type` attribute is `submit`, the type can be omitted if no other type needs to be used. Historical browser versions may have different standard `type` values.

Firefox for Android, by default, sets a `background-image` gradient on all **button** elements. This can be disabled using `background-image: none`.

Firefox will, unlike other browsers, by default, [persist the dynamic disabled state](http://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing) of a **button** across page loads. Setting the value of the `autocomplete` attribute to `off` disables this feature. See [Mozilla Bug \#654072](https://bugzilla.mozilla.org/show_bug.cgi?id=654072).

### Clicking and focus

Whether clicking on a **button** causes it to (by default) become focused varies by browser and OS.

Does clicking on a **button** give it the focus?:

Desktop Browsers
:   Windows 8.1
Firefox 30.0
:   Yes
Chrome 35
:   Yes
Safari 7.0.5
:   N/A
Internet Explorer 11
:   Yes
Presto (Opera 12)
:   Yes

 Does tapping on a **button** give it the focus?:

Mobile Browsers
:   iOS 7.1.2
Safari Mobile
:   No (even with a [`tabindex`](/html/attributes/tabIndex))
Chrome 35
:    ???

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-button-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/forms.html#the-button-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-BUTTON)
:   W3C Recommendation

## See also

### Related articles

#### Document Structure

-   **button**

-   [button](/html/elements/button/ja)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [main](/html/elements/main)

-   [nav](/html/elements/nav)

-   [p](/html/elements/p)

-   [section](/html/elements/section)

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [HTMLAudioElement](/dom/HTMLAudioElement)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   [HTML Elements](/html/elements)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   **button**

-   [button](/html/elements/button/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

<!-- -->

    … further results

### Other articles

-   [**input type="button"**](/html/elements/input/type/button)
-   [**input type="submit"**](/html/elements/input/type/submit)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[\<button\> on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button) Article]

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

