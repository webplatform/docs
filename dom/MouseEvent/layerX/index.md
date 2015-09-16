---
title: 'layerX'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.layerX](https://developer.mozilla.org/en-US/docs/Web/API/event.layerX) Article]'
  - 'Microsoft Developer Network: [[event.layerX](http://msdn.microsoft.com/en-us/library/ie/gg130967(v=vs.85).aspx) Article]'
notes:
  - 'compatibility, clean-up of MSDN content to provide neutral context for non-standard property'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MouseEvent
    href: /dom/MouseEvent
summary: 'Gets the x-coordinate of the mouse pointer, relative to the last positioned ancestor element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/MouseEvent/layerX

---
## Summary

Gets the x-coordinate of the mouse pointer, relative to the last positioned ancestor element.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## Syntax

``` js
var result = element.layerX;
element.layerX = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

A positioned element is an element whose position property is set to `relative`, `absolute` or `fixed`. For more information about element positioning, see About Element Positioning. **Note**  This property is provided for cross-browser compatibility. Use **x** instead.

### Syntax

### Standards information

There are no standards that apply here.
