---
title: removeRange
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.removeRange](https://developer.mozilla.org/en-US/docs/Web/API/Selection.removeRange) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Selection
    href: /dom/Selection
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Selection
standardization_status: 'W3C Working Draft'
summary: 'Removes a range from a selection.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Selection/removeRange

---
## <span>Summary</span>

Removes a range from a selection.

Method of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## <span>Syntax</span>

``` js
var result = selObj.removeRange(/* see parameter list */);
```

## <span>Parameters</span>

### <span>range</span>

 Data-type
:   Range

 Range to remove.

## <span>Return Value</span>

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

``` js
/* In gecko Programmaticaly, more than one range can be selected.
 * This will remove all ranges except the first. see Compatibility Notes below */
selObj = window.getSelection();
if(selObj.rangeCount > 1) {
 for(var i = 1; i < selObj.rangeCount; i++) {
  selObj.removeRange(selObj.getRangeAt(i));
 }
}
```

## <span>Notes</span>

### <span>Remarks</span>

Windows Internet Explorer 9-11 does not currently support multiple or disjointed selections in standards mode.

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
