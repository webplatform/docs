---
title: parentElement
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: Non-Standard
notes:
  - "Needs a modern example (viz not JScript).\nthis should be with Selection object, not textRange."
summary: 'Retrieves the parent element for the given text range.'
uri: dom/TextRange/parentElement

---
# parentElement

## Summary

Retrieves the parent element for the given text range.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var parentNode = textRange.parentElement();
```

## Return Value

Returns an object of type DOM Node.

Returns the parent element object if successful, or null otherwise.

## Examples

This example uses the **parentElement** method to retrieve the parent element for the text range created from the current selection, and display the tag name of the element.

``` {.js}
<SCRIPT LANGUAGE="JScript">
var sel = document.selection;
var rng = sel.createRange();
var el = rng.parentElement();
alert(el.tagName);
</SCRIPT>
```

## Notes

### Remarks

The parent element is the element that completely encloses the text in the range. If the text range spans text in more than one element, this method returns the smallest element that encloses all the elements. When you insert text into a range that spans multiple elements, the text is placed in the parent element rather than in any of the contained elements.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[parentElement Method](http://msdn.microsoft.com/en-us/library/ie/ms536654(v=vs.85).aspx) Article]

