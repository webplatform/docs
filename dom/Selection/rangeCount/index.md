---
title: rangeCount
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the number of ranges in a selection'
uri: dom/Selection/rangeCount

---
# rangeCount

## Summary

Returns the number of ranges in a selection

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Selection](/dom/Selection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var rangecount = selObj.rangeCount;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The number of ranges in a selection.

## Examples

``` {.js}
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.rangeCount](https://developer.mozilla.org/en-US/docs/Web/API/Selection.rangeCount) Article]

Portions of this content come from the Microsoft Developer Network: [[rangeCount Property](http://msdn.microsoft.com/en-us/library/ie/ff974693(v=vs.85).aspx) Article]

