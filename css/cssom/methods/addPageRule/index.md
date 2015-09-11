---
title: addPageRule
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Not implemented and not specified anywhere; deletion candidate.'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/cssom/styleSheet
    href: /css/cssom/styleSheet
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /css/cssom/styleSheet
summary: 'Not implemented anywhere. Non standard.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: css/cssom/methods/addPageRule

---
## <span>Summary</span>

Not implemented anywhere. Non standard.

Method of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## <span>Syntax</span>

``` js
var number = stylesheet.addPageRule(/* see parameter list */);
```

## <span>Parameters</span>

### <span>selector</span>

 Data-type
:   String

 A page selector.

### <span>style</span>

 Data-type
:   String

 This style takes the same form as an inline style specification. For example, "`color:blue`" is a valid style parameter.

### <span>index</span>

 Data-type
:   Number

 The zero-based position in the [**pages**](/css/cssom/pages) collection where the new [**page**](/css/cssom/page) object should be placed.

## <span>Return Value</span>

Returns an object of type NumberNumber

Always returns -1.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Each [**page**](/css/cssom/page) object represents a style sheet that corresponds to a **@page** rule in the document.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `styleSheet`
