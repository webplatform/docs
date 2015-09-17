---
title: 'rangeCount'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.rangeCount](https://developer.mozilla.org/en-US/docs/Web/API/Selection.rangeCount) Article]'
  - 'Microsoft Developer Network: [[rangeCount Property](http://msdn.microsoft.com/en-us/library/ie/ff974693(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Selection
    href: /dom/Selection
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Selection
standardization_status: 'W3C Working Draft'
summary: 'Returns the number of ranges in a selection'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Selection/rangeCount

---
## Summary

Returns the number of ranges in a selection

Property of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

**Note**: This property is read-only.

``` js
var rangecount = selObj.rangeCount;
```

## Return Value

Returns an object of type NumberNumber

The number of ranges in a selection.

## Examples

``` js
var selObj=window.selection();
var rangecount=selObj.rangeCount;
```

## Notes

### Remarks

Windows Internet Explorer 9-11 does not currently support multiple or disjointed selections in standards mode. This property always returns a 1 with a valid selection. It returns a 0 if [**removeRange**](/dom/Selection/removeRange) or [**removeAllRanges**](/dom/Selection/removeAllRanges) have been applied, though calling [**isCollapsed**](/dom/Selection/isCollapsed) is recommended instead to detect an empty range.

Before the user has clicked a freshly loaded page, the rangeCount is 0. A user can normally only select one range at a time, so the rangeCount will usually be 1. Scripting can be used (currently) in Gecko to make the selection contain more than 1 range.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
