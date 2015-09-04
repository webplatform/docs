---
title: usedCharset
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'The character set used to decode external script references.'
uri: css/cssom/properties/usedCharset

---
# usedCharset

## Summary

The character set used to decode external script references.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.usedCharset;
element.usedCharset = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The character set used to decode external script references is based on a number of factors, including the value of the [**charset**](/html/attributes/charset) attribute specified for **script** elements, [byte order marks](http://go.microsoft.com/fwlink/?LinkId=212747), and [HTTP headers](http://go.microsoft.com/fwlink/?LinkId=212748).

### Syntax

## See also

### Related pages (MSDN)

-   `script`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

