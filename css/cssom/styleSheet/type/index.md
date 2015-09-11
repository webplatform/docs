---
title: type
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/styleSheet
    href: /css/cssom/styleSheet
summary: 'The type of a document''s stylesheet.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/styleSheet/type

---
## <span>Summary</span>

The type of a document's stylesheet.

Property of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## <span>Syntax</span>

``` js
var result = element.type;
element.type = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

This property can be any string, including an empty string. Style sheets having any type other than "text/css" are not supported for Microsoft Internet Explorer 4.0. This property can be any string, including an empty string.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `styleSheet`
