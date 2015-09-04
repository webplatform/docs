---
title: clear
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Out of Date'
notes:
  - "clear() is not a method of the HTMLSelection Object.\nref: http://msdn.microsoft.com/en-us/library/ie/ff974359(v=vs.85).aspx\n\nPlease Delete"
summary: "The clear() method is not in HTMLSelection Object.\nUse the removeAllRanges Method instead.\n"
uri: dom/Selection/clear

---
# clear

## Summary

The clear() method is not in HTMLSelection Object. Use the removeAllRanges Method instead.

*Method of [dom/Selection](/dom/Selection)*

## Syntax

``` {.js}
var object = object.clear();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

use removeAllRanges() instead.

``` {.js}
var selObj = window.getSelection();

if(selObj.rangeCount > 0) selObj.removeAllRanges();
```

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

