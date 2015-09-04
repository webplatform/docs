---
title: initEvent
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new generic event that the  createEvent method created.'
uri: dom/Event/initEvent

---
# initEvent

## Summary

Initializes a new generic event that the createEvent method created.

*Method of [dom/Event](/dom/Event)*

## Syntax

``` {.js}
 event.initEvent(eventType, canBubble, cancelable);
```

## Parameters

### eventType

 Data-typeÂ
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

### canBubble

 Data-typeÂ
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### cancelable

 Data-typeÂ
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

## Return Value

No return value

## Examples

The following code example creates a custom event that bubbles but cannot be canceled.

``` {.js}
var evt = document.createEvent("Event");
evt.initEvent("custom", true, false);
document.getElementById('target').dispatchEvent(evt);
```

## Usage

     Use this method before the   dispatchEvent method dispatches the event object, to set some properties of the event.

## Notes

After the event is dispatched, its properties cannot be changed.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages (MSDN)

-   `SVGZoomEvent`
-   `BeforeUnloadEvent`
-   `CompositionEvent`
-   `CustomEvent`
-   `Event`
-   `DragEvent`
-   `FocusEvent`
-   `KeyboardEvent`
-   `MessageEvent`
-   `MouseEvent`
-   `WheelEvent`
-   `MutationEvent`
-   `StorageEvent`
-   `TextEvent`
-   `UIEvent`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

