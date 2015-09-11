---
title: defaultChecked
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLInputElement
    href: /dom/HTMLInputElement
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/HTMLInputElement
standardization_status: 'W3C Recommendation'
summary: 'Gets whether the checked HTML attribute is present on the element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLInputElement/defaultChecked

---
## <span>Summary</span>

Gets whether the checked HTML attribute is present on the element.

Property of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var initiallyChecked = checkboxElement.defaultChecked;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the **checked** HTML attribute is present on the element.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

-   This property reflects the value of the **checked** HTML attribute.
-   This property can be changed programmatically, however, doing so has no effect on the appearance of the check box or radio button or on how forms are submitted - if the [**checked**](/dom/HTMLInputElement/checked) property has been changed by a user or by a script.

## <span>Related specifications</span>

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `checked`
