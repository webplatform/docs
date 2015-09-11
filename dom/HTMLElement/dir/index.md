---
title: dir
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, compatibility, standards, clean-up of MSDN sections'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
standardization_status: Unknown
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/dir

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.dir;
element.dir = value;
```

## <span>Notes</span>

### <span>Remarks</span>

Unless explicitly set, the **dir** property has no return value when accessed in script. The **dir** property does not affect alphanumeric characters in Latin documents. These characters always render **ltr**. However, the property does affect punctuation characters in Latin documents. For example, punctuation marks such as periods and question marks will render to the left of a sentence when the **dir** property is set to **rtl**. The value of **dir** property has no effect on the orientation of coordinates for an object's positioning properties. For example, the [**left**](/css/properties/left) property and the [**right**](/css/properties/right) property perform the same placement in both cases. However, when both the **left** and **right** properties are specified, the **left** property takes precedence when the **dir** property is set to **ltr**. Likewise, the **right** property takes precedence when the **dir** property is set to **rtl**.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Document`
-   `Reference`
-   `direction`
-   `Conceptual`
-   `HTML Character Sets`
