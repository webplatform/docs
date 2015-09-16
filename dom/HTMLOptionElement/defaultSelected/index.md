---
title: 'defaultSelected'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLOptionElement
    href: /dom/HTMLOptionElement
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/HTMLOptionElement
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the value of the selected HTML attribute.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLOptionElement/defaultSelected

---
## Summary

Gets or sets the value of the selected HTML attribute.

Property of [dom/HTMLOptionElement](/dom/HTMLOptionElement)[dom/HTMLOptionElement](/dom/HTMLOptionElement)

## Syntax

``` js
var initiallySelected = option.defaultSelected;
option.defaultSelected = value;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the **selected** HTML attribute is present.

**Needs Examples**: This section should include examples.

## Notes

The property can be changed programmatically, but doing so has no effect on the appearance of the option or the submitted value - if the [**selected**](/html/attributes/selected) property has been changed by a user or by a script. The property does change the appearance of the selected option if the form is reset.

## Related specifications

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## See also

### Related pages

-   selected[selected](/html/attributes/selected)
