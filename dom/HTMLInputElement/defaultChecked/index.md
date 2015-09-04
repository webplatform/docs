---
title: defaultChecked
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'examples, compatibility'
summary: 'Gets whether the checked HTML attribute is present on the element.'
uri: dom/HTMLInputElement/defaultChecked

---
# defaultChecked

## Summary

Gets whether the checked HTML attribute is present on the element.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLInputElement](/dom/HTMLInputElement)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var initiallyChecked = checkboxElement.defaultChecked;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the **checked** HTML attribute is present on the element.

**Needs Examples**: This section should include examples.

## Notes

-   This property reflects the value of the **checked** HTML attribute.
-   This property can be changed programmatically, however, doing so has no effect on the appearance of the check box or radio button or on how forms are submitted - if the [**checked**](/dom/HTMLInputElement/checked) property has been changed by a user or by a script.

## Related specifications

Specification
:   Status
[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## See also

### Related pages (MSDN)

-   `checked`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

