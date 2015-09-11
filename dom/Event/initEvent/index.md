---
title: initEvent
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Event
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Initializes a new generic event that the  createEvent method created.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Event/initEvent

---
## <span>Summary</span>

Initializes a new generic event that the createEvent method created.

Method of [dom/Event](/dom/Event)[dom/Event](/dom/Event)

## <span>Syntax</span>

``` js
 event.initEvent(eventType, canBubble, cancelable);
```

## <span>Parameters</span>

### <span>eventType</span>

 Data-type
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property.

### <span>canBubble</span>

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### <span>cancelable</span>

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

## <span>Return Value</span>

No return value

## <span>Examples</span>

The following code example creates a custom event that bubbles but cannot be canceled.

``` js
var evt = document.createEvent("Event");
evt.initEvent("custom", true, false);
document.getElementById('target').dispatchEvent(evt);
```

## <span>Usage</span>

     Use this method before the   dispatchEvent method dispatches the event object, to set some properties of the event.

## <span>Notes</span>

After the event is dispatched, its properties cannot be changed.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## <span>See also</span>

### <span>Related pages (MSDN)</span>

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
