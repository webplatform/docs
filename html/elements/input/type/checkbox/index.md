---
title: 'checkbox'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: checkbox
  topic: html
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
summary: 'The checkbox type of the &lt;input&gt; element represents a state or option that can be toggled.'
tags:
  - Pages_using_duplicate_arguments_in_template_calls
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/defaultChecked
uri: html/elements/input/type/checkbox

---
## Summary

The checkbox type of the &lt;input&gt; element represents a state or option that can be toggled.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

``` html
<input type="checkbox" name="vehicle" value="Bike"> I have a bike<br>
<input type="checkbox" name="vehicle" value="Car"> I have a car
```

## Notes

### Remarks

When an **input type=checkbox** element is selected, a name/value pair is submitted with the **form**. The default value of **input type=checkbox** is on. The [**height**](/css/properties/height) and [**width**](/css/properties/width) styles are exposed to the **input type=checkbox** element. The size of the element is set based on the values provided by the author, subject to a particular minimum. The size is calculated as follows:

-   If the [**height**](/css/properties/height) or [**width**](/css/properties/width) is greater than 20 pixels, the padding around the check box is set to 4 pixels, and the inner height or width is set to 8 pixels.
-   If the [**height**](/css/properties/height) or [**width**](/css/properties/width) is less than 20 pixels but greater than 13 pixels, the padding around the check box is equal to one half the specified **height** or **width** minus 13. For example, if the specified **width** of the check box is 17, the equation would be: (17-13)/2.
-   If the [**height**](/css/properties/height) or [**width**](/css/properties/width) is less than 12 pixels, the padding around the check box is set to 0 and the inner width is set to the value specified by the author.

**Note**  For code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site. In IE8 Standards mode and later, inserting an **input type=checkbox** object into the Document Object Model (DOM) tree does not reset the [**defaultChecked**](/w/index.php?title=dom/properties/defaultChecked&action=edit&redlink=1) property. For more information, see Defining Document Compatibility.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4

### HTML information

{

## See also

### Related pages

-   `input`
