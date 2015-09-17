---
title: 'SVGZoom'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /svg/objects/SVGElement
tags:
  - API_Objects
  - DOM
  - Needs_Summary
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/initEvent
    - dom/methods/createEvent
    - dom/methods/initUIEvent
    - dom/methods/preventDefault
    - dom/methods/stopImmediatePropagation
    - dom/methods/stopPropagation
    - dom/properties/bubbles
    - dom/properties/cancelable
    - dom/methods/cancelBubble
    - dom/properties/currentTarget
    - dom/properties/defaultPrevented
    - dom/properties/detail
    - dom/properties/eventPhase
    - dom/properties/isTrusted
    - dom/properties/srcElement
    - dom/properties/target
    - dom/properties/timeStamp
    - 'dom/properties/type (event)'
    - dom/properties/view
uri: svg/objects/SVGZoom

---
Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from SVGElement

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The **zoom** event occurs when a user initiates an action that causes the current view of the SVG document (or SVGdocument fragment) to be rescaled (including any change to the [**svg**](/svg/elements/svg) element's [**currentScale**](/svg/properties/currentScale) property).

**Note:** A zoom event applies only to the outermost [**svg**](/svg/elements/svg) element.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Scripting](http://go.microsoft.com/fwlink/p/?linkid=204745), Section 18.5.2

### Members

The **SVGZoomEvent** object has these methods:

-   [**initEvent**](/w/index.php?title=dom/methods/initEvent&action=edit&redlink=1): Initializes a new generic event that the [**createEvent**](/w/index.php?title=dom/methods/createEvent&action=edit&redlink=1) method created.
-   [**initUIEvent**](/w/index.php?title=dom/methods/initUIEvent&action=edit&redlink=1): Initializes a new user interface event that the [**createEvent**](/w/index.php?title=dom/methods/createEvent&action=edit&redlink=1) method created.
-   [**preventDefault**](/w/index.php?title=dom/methods/preventDefault&action=edit&redlink=1): Cancels the default action of an event.
-   [**stopImmediatePropagation**](/w/index.php?title=dom/methods/stopImmediatePropagation&action=edit&redlink=1): Prevents any further propagation of an event.
-   [**stopPropagation**](/w/index.php?title=dom/methods/stopPropagation&action=edit&redlink=1): Prevents propagation of an event beyond the current target.

The **SVGZoomEvent** object has these properties:

-   [**bubbles**](/w/index.php?title=dom/properties/bubbles&action=edit&redlink=1): Gets a value that indicates whether an event propagates up from the event target.
-   [**cancelable**](/w/index.php?title=dom/properties/cancelable&action=edit&redlink=1): Gets a value that indicates whether you can cancel an event's default action.
-   [**cancelBubble**](/w/index.php?title=dom/methods/cancelBubble&action=edit&redlink=1): Gets or sets a value that indicates whether an event should be stopped from propagating up from the current target.
-   [**currentTarget**](/w/index.php?title=dom/properties/currentTarget&action=edit&redlink=1): Gets the event target that is currently being processed.
-   [**defaultPrevented**](/w/index.php?title=dom/properties/defaultPrevented&action=edit&redlink=1): Gets a value that indicates whether the default action should be canceled.
-   [**detail**](/w/index.php?title=dom/properties/detail&action=edit&redlink=1): Gets additional information about an event.
-   [**eventPhase**](/w/index.php?title=dom/properties/eventPhase&action=edit&redlink=1): Gets the event phase that is being evaluated.
-   [**isTrusted**](/w/index.php?title=dom/properties/isTrusted&action=edit&redlink=1): Gets a value that indicates whether a trusted event source created an event.
-   [**newScale**](/svg/properties/newScale): Gets the new scale value of a zoom event.
-   [**newTranslate**](/svg/properties/newTranslate): Gets the new translation values of a zoom event.
-   [**previousScale**](/svg/properties/previousScale): Gets the previous scale value of a zoom event.
-   [**previousTranslate**](/svg/properties/previousTranslate): Gets the previous translation values of a zoom event.
-   [**srcElement**](/w/index.php?title=dom/properties/srcElement&action=edit&redlink=1): Gets the element that the event was originally dispatched to. Compare to [**target**](/w/index.php?title=dom/properties/target&action=edit&redlink=1).
-   [**target**](/w/index.php?title=dom/properties/target&action=edit&redlink=1): Gets the element that is the target of the event.
-   [**timeStamp**](/w/index.php?title=dom/properties/timeStamp&action=edit&redlink=1): Gets the time, in milliseconds, when an event occurred.
-   [**type**](/w/index.php?title=dom/properties/type_(event)&action=edit&redlink=1): Gets the name of an event.
-   [**view**](/w/index.php?title=dom/properties/view&action=edit&redlink=1): Gets the **window** object that an event is generated from.
