---
title: 'defaultValue'
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
    value: String
    href: /dom/HTMLInputElement
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the value of the value HTML attribute.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLInputElement/defaultValue

---
## Summary

Gets or sets the value of the value HTML attribute.

Property of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## Syntax

``` js
var defaultValue = inputElement.defaultValue;
inputElement.defaultValue = value;
```

## Return Value

Returns an object of type StringString

The value of the **value** HTML attribute.

**Needs Examples**: This section should include examples.

## Notes

The value of the property can be changed programmatically, but doing so has no effect on the appearance of the object or the submitted value - if the [value](/dom/HTMLElement/value) property has been changed by a user or by a script. It does, however, change the initial value of the object when the form is reset.

## Related specifications

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## See also

### Related pages

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
