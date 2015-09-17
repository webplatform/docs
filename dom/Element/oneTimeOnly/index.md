---
title: 'oneTimeOnly'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, and compat'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/oneTimeOnly

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.;
element. = value;
```

## Notes

### Remarks

When an object created with [**createObjectURL**](/apis/file/URL/createObjectURL) uses this attribute set to true, the object is only used once. The [**revokeObjectURL**](/apis/file/URL/revokeObjectURL) method does not need to be used on the object.

### Syntax

## See also

### Related pages

-   createObjectURL[createObjectURL](/apis/file/URL/createObjectURL)
-   revokeObjectURL[revokeObjectURL](/apis/file/URL/revokeObjectURL)
-   ObjectURLOptions[ObjectURLOptions](/apis/file/ObjectURLOptions)
