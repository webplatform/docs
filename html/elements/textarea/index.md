---
title: 'textarea'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: textarea
  topic: html
notes:
  - 'Should have automatic child links generated.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTextAreaElement](/dom/HTMLTextAreaElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "The textarea tag defines a multi-line text input control.\n"
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/textarea

---
## Summary

The textarea tag defines a multi-line text input control.

A text area can hold an unlimited number of characters, and the text renders in a fixed-width font (usually Courier).

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTextAreaElement](/dom/HTMLTextAreaElement)

Internationalization topics related to the `a` element:

-   [Setting direction on block elements](http://localhost/International/techniques/authoring-html#blocks)
-   [Managing text direction in form controls](http://localhost/International/techniques/authoring-html#formdir)

## Examples

This example uses the `textarea` element to set the cascading style sheets (CSS) [**overflow**](/css/properties/overflow) attribute to `hidden` to remove the scroll bars from the `textarea`.

``` html
<textarea style="overflow:hidden" id="txtComments">
   The patient is in stable condition after suffering an attack of
   the insatiable munchies.
</textarea>
```

## Usage

     To cater for international users see: Managing text direction in form controls

## HTML Attributes

 Global attributes: accesskey, class, contenteditable, dir, hidden, id, lang, spellcheck, style, tabindex, title, translate
:   See [global attributes](/html/global_attributes).

 `autofocus` = boolean
:   Allows the author to indicate that a control is to be focused as soon as the page is loaded

 `cols` = non-negative integer
:   specifies the expected maximum number of characters per line. by default, it is 20.

 `disabled` = boolean
:   If present, make the control non-interactive and to prevent its value from being submitted.

 `form` = the ID of a form element in the element's owner
:   Associate the textarea element with its form owner.
    By default, the textarea element is associated with its nearest ancestor form element.

 `name` = unique name
:   Represents the element's name.

 `placeholder` = sample value or a brief description of the expected format
:   Represents a hint (a word or short phrase) intended to aid the user with data entry.
    The placeholder attribute should not be used as an alternative to a label.

 `readonly` = boolean
:   Control whether the text can be edited by the user or not.

 `required` = boolean
:   When specified, the user will be required to enter a value before submitting the form.

 `rows` = valid non-negative integer
:   Specifies the number of lines to show. by defult, it is 2.

 `wrap` = "soft"/ "hard"
:   soft
    :   The Soft state indicates that the text in the textarea is not to be wrapped when it is submitted (though it can still be wrapped in the rendering).
    hard
    :   The Hard state indicates that the text in the textarea is to have newlines added by the user agent so that the text is wrapped when it is submitted.
        If the element's wrap attribute is in the Hard state, the cols attribute must be specified.

## Notes

### Remarks

The default font is fixed pitch.

Firefox for Android, by default, sets a `background-image` gradient on all **textarea** elements. This can be disabled using `background-image: none`.

Safari Mobile for iOS applies a default style of [`opacity`](/css/properties/opacity)`: 0.4` to disabled **`textarea`** elements. Other major browsers don't currently share this particular default style.

**Security Warning:  **Using this object incorrectly can compromise the security of your application. When submitting text through `textarea` over an intranet or the Internet, validating the text string is recommended. For instance, you might validate the string for a restricted set of known, good values (such as letters and numbers) and ignore the rest.

### Default CSS

    white-space: pre-wrap;
    text-indent: initial;

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-textarea-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-textarea-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-TEXTAREA)
:   W3C Recommendation
