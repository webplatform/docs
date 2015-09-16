---
title: addRange
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.addRange](https://developer.mozilla.org/en-US/docs/Web/API/Selection.addRange) Article]'
  - 'Microsoft Developer Network: [[addRange Method](http://msdn.microsoft.com/en-us/library/ie/ff975172(v=vs.85).aspx) Article]'
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
summary: 'Adds a Range to the current selection.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Selection/addRange

---
## Summary

Adds a Range to the current selection.

Method of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

``` js
var result = selObj.addRange(/* see parameter list */);
```

## Parameters

### range

 Data-type
:   Range

 Range to add.

## Return Value

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

``` js
/* Select all STRONG elements in an HTML document */

var strongs = document.getElementsByTagName('strong');
var selObj = window.getSelection();

if(selObj.rangeCount > 0) selObj.removeAllRanges();

for(var i = 0; i < strongs.length; i++) {
  var range = document.createRange();
  range.selectNode(strongs[i]);
  selObj.addRange(range);
}
```

``` js
function selectElements(tagName){
var els = document.getElementsByTagName(tagName);
var selObj = window.getSelection();
if(selObj.rangeCount > 0) selObj.removeAllRanges();
        for(var i = 0; i < els.length; i++) {
          var range = document.createRange();
          range.selectNode(els[i]);
          selObj.addRange(range);
        }
   }
```

## Notes

### Remarks

Windows Internet Explorer 9 and higher and Webkit browser do not currently support multiple or disjointed selections in standards mode. If **addRange** is applied to a selection that already contains a Range, the new Range is not added.

### Syntax

selObj.addRange(range)

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
