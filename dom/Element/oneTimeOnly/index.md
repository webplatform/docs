---
title: oneTimeOnly
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
  - API
  - Object
  - Properties
  - DOM
uri: dom/Element/oneTimeOnly

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var result = element.;
element. = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

When an object created with [**createObjectURL**](/apis/file/URL/createObjectURL) uses this attribute set to true, the object is only used once. The [**revokeObjectURL**](/apis/file/URL/revokeObjectURL) method does not need to be used on the object.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `createObjectURL`
-   `revokeObjectURL`
-   `ObjectURLOptions`
