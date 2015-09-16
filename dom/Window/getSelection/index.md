---
title: getSelection
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[getSelection](https://developer.mozilla.org/en-US/docs/Web/API/Window.getSelection) Article]'
  - 'Microsoft Developer Network: [[getSelection Method](http://msdn.microsoft.com/en-us/library/ie/ff975169(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
  return_type:
    predicate: 'Returns an object of type  '
    value: Object
    href: /dom/Window
standardization_status: 'W3C Recommendation'
summary: 'Returns a Selection object that represents the current selection of the document.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/getSelection

---
## Summary

Returns a Selection object that represents the current selection of the document.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var selection = window.getSelection();
```

## Return Value

Returns an object of type ObjectObject

A [Selection](/dom/Selection) object that represents the currently selected text in the window.

## Examples

``` js
function foo() {
    var selObj = window.getSelection();
    alert(selObj);
    var selRange = selObj.getRangeAt(0);
    // do stuff with the range
}
```

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 6.6.1
