---
title: usedCharset
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/properties
    href: /css/cssom/properties
summary: 'The character set used to decode external script references.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/usedCharset

---
## <span>Summary</span>

The character set used to decode external script references.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## <span>Syntax</span>

``` js
var result = element.usedCharset;
element.usedCharset = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The character set used to decode external script references is based on a number of factors, including the value of the [**charset**](/html/attributes/charset) attribute specified for **script** elements, [byte order marks](http://go.microsoft.com/fwlink/?LinkId=212747), and [HTTP headers](http://go.microsoft.com/fwlink/?LinkId=212748).

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `script`
