---
title: 'defaultChecked'
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
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/HTMLInputElement/defaultChecked

---
## Summary

Gets whether the checked HTML attribute is present on the element.

Property of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## Syntax

**Note**: This property is read-only.

``` js
var initiallyChecked = checkboxElement.defaultChecked;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the **checked** HTML attribute is present on the element.

## Notes

-   This property reflects the value of the **checked** HTML attribute.
-   This property can be changed programmatically, however, doing so has no effect on the appearance of the check box or radio button or on how forms are submitted - if the [**checked**](/dom/HTMLInputElement/checked) property has been changed by a user or by a script.

## Related specifications

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## See also

### Related pages

-   checked[checked](/html/attributes/checked)
