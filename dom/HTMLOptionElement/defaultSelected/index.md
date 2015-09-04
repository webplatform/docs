---
title: defaultSelected
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'examples, compatibility'
summary: 'Gets or sets the value of the selected HTML attribute.'
uri: dom/HTMLOptionElement/defaultSelected

---
# defaultSelected

## Summary

Gets or sets the value of the selected HTML attribute.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLOptionElement](/dom/HTMLOptionElement)</span></span>

## Syntax

``` {.js}
var initiallySelected = option.defaultSelected;
option.defaultSelected = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the **selected** HTML attribute is present.

**Needs Examples**: This section should include examples.

## Notes

The property can be changed programmatically, but doing so has no effect on the appearance of the option or the submitted value - if the [**selected**](/html/attributes/selected) property has been changed by a user or by a script. The property does change the appearance of the selected option if the form is reset.

## Related specifications

Specification
:   Status
[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## See also

### Related pages (MSDN)

-   `selected`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

