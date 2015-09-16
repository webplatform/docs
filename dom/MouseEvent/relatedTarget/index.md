---
title: 'relatedTarget'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.relatedTarget](https://developer.mozilla.org/en-US/docs/Web/API/event.relatedTarget) Article]'
  - 'Microsoft Developer Network: [[event.relatedTarget](http://msdn.microsoft.com/en-us/library/ie/ff974881(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[event.relatedTarget samples](http://www.html5rocks.com/en/search?q=event.relatedTarget) article]'
notes:
  - 'Needs an example....'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MouseEvent
    href: /dom/MouseEvent
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: "Gets the secondary element that is involved in an event.\nThe relatedTarget property is used to find the other element, if any, involved in an event. Events like mouseover are oriented around a certain target, but also involve a secondary target, such as the target that is exited as the mouseover event fires for the primary target.\n"
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
uri: dom/MouseEvent/relatedTarget

---
## Summary

Gets the secondary element that is involved in an event. The relatedTarget property is used to find the other element, if any, involved in an event. Events like mouseover are oriented around a certain target, but also involve a secondary target, such as the target that is exited as the mouseover event fires for the primary target.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var relatedTargetElement = event.relatedTarget;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The secondary element that is involved in an event.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine the secondary element that is involved in the event.

The secondary element depends on the type of event:

-   In [**mouseover**](/dom/MouseEvent/mouseover) events, the secondary element is the element that the mouse pointer left.
-   In [**mouseout**](/dom/MouseEvent/mouseout) events, the secondary element is the element that the mouse pointer entered.
-   In [**focusin**](/dom/FocusEvent/focusin) events, the secondary element is the element that lost focus.
-   In [**focusout**](/dom/FocusEvent/focusout) events, the secondary element is the element that gained focus.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
