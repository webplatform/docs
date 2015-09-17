---
title: 'collapse'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.collapse](https://developer.mozilla.org/en-US/docs/Web/API/Range.collapse) Article]'
  - 'Microsoft Developer Network: [[collapse Method](http://msdn.microsoft.com/en-us/library/ie/ff975439(v=vs.85).aspx) Article]'
notes:
  - 'nilladic function.... no return value...'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Collapses (or removes) a range by moving the insertion point to the beginning or end of the current range.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Range/collapse

---
## Summary

Collapses (or removes) a range by moving the insertion point to the beginning or end of the current range.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

``` js
var result = range.collapse(/* see parameter list */);
```

## Parameters

### toStart

 Data-type
:   Boolean

(Optional)

Specifies one of the following values:

true (Default). Moves the insertion point to the beginning of the range.

false Moves the insertion point to the end of the range.

## Return Value

Returns an object of type

## Examples

``` js
var range = document.createRange();

var referenceNode = document.getElementsByTagName("div").item(0);
range.selectNode(referenceNode);
range.collapse(true);
```

## Notes

The DOM 'Living Standard' specification now recommends that the default parameter value be false... To retain interoperability across browsers ALWAYS specify the toStart parameter (true

### Syntax

range.collapse(toStart);

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-range-collapse)
:   Living Standard
