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
## Summary

The character set used to decode external script references.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## Syntax

``` js
var result = element.usedCharset;
element.usedCharset = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The character set used to decode external script references is based on a number of factors, including the value of the [**charset**](/html/attributes/charset) attribute specified for **script** elements, [byte order marks](http://go.microsoft.com/fwlink/?LinkId=212747), and [HTTP headers](http://go.microsoft.com/fwlink/?LinkId=212748).

### Syntax

## See also

### Related pages

-   `script`
