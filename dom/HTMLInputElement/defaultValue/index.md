---
title: defaultValue
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'examples, compatibility'
summary: 'Gets or sets the value of the value HTML attribute.'
uri: dom/HTMLInputElement/defaultValue

---
# defaultValue

## Summary

Gets or sets the value of the value HTML attribute.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLInputElement](/dom/HTMLInputElement)</span></span>

## Syntax

``` {.js}
var defaultValue = inputElement.defaultValue;
inputElement.defaultValue = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The value of the **value** HTML attribute.

**Needs Examples**: This section should include examples.

## Notes

The value of the property can be changed programmatically, but doing so has no effect on the appearance of the object or the submitted value - if the [value](/dom/HTMLElement/value) property has been changed by a user or by a script. It does, however, change the initial value of the object when the form is reset.

## Related specifications

Specification
:   Status
[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## See also

### Related pages (MSDN)

-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
-   `input type=hidden`
-   `input type=image`
-   `input type=password`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=text`
-   `textArea`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

