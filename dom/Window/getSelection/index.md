---
title: getSelection
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Returns a Selection object that represents the current selection of the document.'
uri: dom/Window/getSelection

---
# getSelection

## Summary

Returns a Selection object that represents the current selection of the document.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
var selection = window.getSelection();
```

## Return Value

Returns an object of type Object.

A [Selection](/dom/Selection) object that represents the currently selected text in the window.

## Examples

``` {.js}
function foo() {
    var selObj = window.getSelection();
    alert(selObj);
    var selRange = selObj.getRangeAt(0);
    // do stuff with the range
}
```

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 6.6.1

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[getSelection](https://developer.mozilla.org/en-US/docs/Web/API/Window.getSelection) Article]

Portions of this content come from the Microsoft Developer Network: [[getSelection Method](http://msdn.microsoft.com/en-us/library/ie/ff975169(v=vs.85).aspx) Article]

