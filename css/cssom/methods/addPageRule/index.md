---
title: addPageRule
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'Not implemented and not specified anywhere; deletion candidate.'
summary: 'Not implemented anywhere. Non standard.'
uri: css/cssom/methods/addPageRule

---
# addPageRule

## Summary

Not implemented anywhere. Non standard.

*Method of [css/cssom/styleSheet](/css/cssom/styleSheet)*

## Syntax

``` {.js}
var number = stylesheet.addPageRule(/* see parameter list */);
```

## Parameters

### selector

 Data-typeÂ
:   String

 A page selector.

### style

 Data-typeÂ
:   String

 This style takes the same form as an inline style specification. For example, "`color:blue`" is a valid style parameter.

### index

 Data-typeÂ
:   Number

 The zero-based position in the [**pages**](/css/cssom/pages) collection where the new [**page**](/css/cssom/page) object should be placed.

## Return Value

Returns an object of type Number.

Always returns -1.

**Needs Examples**: This section should include examples.

## Notes

Each [**page**](/css/cssom/page) object represents a style sheet that corresponds to a **@page** rule in the document.

## See also

### Related pages (MSDN)

-   `styleSheet`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

