---
title: removeRange
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Removes a range from a selection.'
uri: dom/Selection/removeRange

---
# removeRange

## Summary

Removes a range from a selection.

*Method of [dom/Selection](/dom/Selection)*

## Syntax

``` {.js}
var result = selObj.removeRange(/* see parameter list */);
```

## Parameters

### range

 Data-typeÂ
:   Range

 Range to remove.

## Return Value

Returns an object of type Number.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

``` {.js}
/* In gecko Programmaticaly, more than one range can be selected.
 * This will remove all ranges except the first. see Compatibility Notes below */
selObj = window.getSelection();
if(selObj.rangeCount > 1) {
 for(var i = 1; i < selObj.rangeCount; i++) {
  selObj.removeRange(selObj.getRangeAt(i));
 }
}
```

## Notes

### Remarks

Windows Internet ExplorerÂ 9-11 does not currently support multiple or disjointed selections in standards mode.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.removeRange](https://developer.mozilla.org/en-US/docs/Web/API/Selection.removeRange) Article]

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

