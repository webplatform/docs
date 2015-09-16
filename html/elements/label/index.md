---
title: label
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/accesskey.htm'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLLabelElement](/dom/HTMLLabelElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'Specifies a label for another element on the page.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/click
uri: html/elements/label

---
## Summary

Specifies a label for another element on the page.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLLabelElement](/dom/HTMLLabelElement)

The content of the label provides the caption for the input. The input can be specified in one of two ways:

1.  The input can be identified by the "for" attribute
2.  The input can be a child element of the label

User agents will often focus the cursor on the input element after clicking the associated label.

## HTML Attributes

 `form` = string
:   Associate the fieldset element with its form owner.
 `for` = string
:   Specified to indicate a form control with which the caption is to be associated.
    The attribute's value must be the ID of a labelable form-associated element in the same Document as the label element.

## Examples

This example uses the **LABEL** element and the [**ACCESSKEY**](/html/attributes/accessKey) attribute to set focus on a text box.

``` html
<label for="oCtrlID" accesskey="1">
    #<span style="text-decoration:underline;">1</span>: Press Alt+1 to set focus to textbox
</label>
<input type="text" name="txt1" value="binding sample 1"
       size="20" tabindex="1" id="oCtrlID"/>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/accesskey.htm)

## Notes

### Remarks

To bind a **LABEL** to another control, set the [**FOR**](/html/attributes/dom/for) attribute of the **LABEL** element equal to the [**ID**](/html/attributes/id) of the control. Binding a **LABEL** to the [**NAME**](/html/attributes/name) attribute of the control has no effect. However, to submit a form, you must specify a **NAME** on the control to which the **LABEL** element is being bound. There are two ways to underline the designated access key. The rich text support in the **LABEL** element makes it possible to wrap the **U** element around the character in the label text specified by the [**ACCESSKEY**](/html/attributes/accessKey) attribute. If you prefer to use cascading style sheets (CSS) to apply style formatting, enclose the designated character in a **SPAN** and set the style to `"text-decoration: underline"`. If the user clicks the **LABEL**, the [**onclick**](/w/index.php?title=dom/events/click&action=edit&redlink=1) event fires on the **LABEL** and then on the control specified by the [**htmlFor**](/html/attributes/dom/for) property. Pressing the access key for the **LABEL** sets the focus but does not fire the **onclick** event. Labels cannot be nested.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-label-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-label-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-LABEL)
:   W3C Recommendation
