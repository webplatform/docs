---
title: output
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLOutputElement](/w/index.php?title=dom/HTMLOutputElement&action=edit&redlink=1)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The HTML &lt;output&gt; element represents the result of a calculation.'
tags:
  - Markup
  - Elements
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLOutputElement
uri: html/elements/output

---
## Summary

The HTML &lt;output&gt; element represents the result of a calculation.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLOutputElement](/w/index.php?title=dom/HTMLOutputElement&action=edit&redlink=1)

The HTML \<output\> element represents the result of a calculation.

## Attributes

-   `for` = unordered set of unique space-separated tokens
    Allows an explicit relationship to be made between the result of a calculation and the elements that represent the values that went into the calculation or that otherwise influenced the calculation.
    This attribute must have the value of an ID of an element in the same Document.
-   `form` = the ID of a form element in the element's owner
    Associate the output element with its form owner.
    By default, the output element is associated with its nearest ancestor form element.
-   `name` = unique name
    Represents the element's name.

## Examples

``` html
<form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
    <input type="range" name="b" value="50" /> +
    <input type="number" name="a" value="10" /> =
    <output name="result"></output>
</form>
```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-output-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-output-element)
:   W3C Recommendation

