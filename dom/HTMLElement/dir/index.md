---
title: dir
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'summary, examples, compatibility, standards, clean-up of MSDN sections'
uri: dom/HTMLElement/dir

---
# dir

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.dir;
element.dir = value;
```

## Notes

### Remarks

Unless explicitly set, the **dir** property has no return value when accessed in script. The **dir** property does not affect alphanumeric characters in Latin documents. These characters always render **ltr**. However, the property does affect punctuation characters in Latin documents. For example, punctuation marks such as periods and question marks will render to the left of a sentence when the **dir** property is set to **rtl**. The value of **dir** property has no effect on the orientation of coordinates for an object's positioning properties. For example, the [**left**](/css/properties/left) property and the [**right**](/css/properties/right) property perform the same placement in both cases. However, when both the **left** and **right** properties are specified, the **left** property takes precedence when the **dir** property is set to **ltr**. Likewise, the **right** property takes precedence when the **dir** property is set to **rtl**.

### Syntax

## See also

### Related pages (MSDN)

-   `Document`
-   `Reference`
-   `direction`
-   `Conceptual`
-   `HTML Character Sets`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

