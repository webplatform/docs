---
title: parentElement
attributions:
  - 'Microsoft Developer Network: [[parentElement Method](http://msdn.microsoft.com/en-us/library/ie/ms536654(v=vs.85).aspx) Article]'
notes:
  - "Needs a modern example (viz not JScript).\nthis should be with Selection object, not textRange."
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Retrieves the parent element for the given text range.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/parentElement

---
## <span>Summary</span>

Retrieves the parent element for the given text range.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## <span>Syntax</span>

``` js
var parentNode = textRange.parentElement();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Returns the parent element object if successful, or null otherwise.

## <span>Examples</span>

This example uses the **parentElement** method to retrieve the parent element for the text range created from the current selection, and display the tag name of the element.

``` js
<SCRIPT LANGUAGE="JScript">
var sel = document.selection;
var rng = sel.createRange();
var el = rng.parentElement();
alert(el.tagName);
</SCRIPT>
```

## <span>Notes</span>

### <span>Remarks</span>

The parent element is the element that completely encloses the text in the range. If the text range spans text in more than one element, this method returns the smallest element that encloses all the elements. When you insert text into a range that spans multiple elements, the text is placed in the parent element rather than in any of the contained elements.