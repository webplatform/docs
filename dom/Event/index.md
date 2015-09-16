---
title: 'Event'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Represents an event.'
tags:
  - API
  - Objects
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/MouseWheelEvent
uri: dom/Event

---
## Summary

Represents an event.

## Properties

API Name
:   Summary

[bubbles](/dom/Event/bubbles)
:   Gets a value that indicates whether an event propagates up from the event target.

[cancelable](/dom/Event/cancelable)
:   Gets a value that indicates whether you can cancel an event's default action.

[currentTarget](/dom/Event/currentTarget)
:   Gets the event target that is currently being processed.

[defaultPrevented](/dom/Event/defaultPrevented)
:   Gets whether the default action should be canceled.

[eventPhase](/dom/Event/eventPhase)
:   Gets the event phase that is being evaluated.

[isTrusted](/dom/Event/isTrusted)
:   Gets a value that indicates whether a trusted event source created an event.

[target](/dom/Event/target)
:   Gets the element that is the original target of the event.

[timeStamp](/dom/Event/timeStamp)
:   Gets the time, in milliseconds, when an event occurred.

[type](/dom/Event/type)
:   Gets the name of an event.

## Methods

API Name
:   Summary

[initEvent](/dom/Event/initEvent)
:   Initializes a new generic event that the [**createEvent**](/dom/Document/createEvent) method created.

[preventDefault](/dom/Event/preventDefault)
:   Cancels the default action of an event, if possible.

[stopImmediatePropagation](/dom/Event/stopImmediatePropagation)
:   Prevents any further propagation of an event.

[stopPropagation](/dom/Event/stopPropagation)
:   Prevents propagation of an event beyond the current target.

## Events

API Name
:   Summary

[DOMContentLoaded](/dom/Event/DOMContentLoaded)
:

[afterprint](/dom/Event/afterprint)
:

[afterupdate](/dom/Event/afterupdate)
:

[beforeactivate](/dom/Event/beforeactivate)
:

[beforecopy](/dom/Event/beforecopy)
:

[beforecut](/dom/Event/beforecut)
:

[beforeeditfocus](/dom/Event/beforeeditfocus)
:

[beforepaste](/dom/Event/beforepaste)
:

[beforeprint](/dom/Event/beforeprint)
:

[beforeunload](/dom/Event/beforeunload)
:

[beforeupdate](/dom/Event/beforeupdate)
:

[bounce](/dom/Event/bounce)
:

[cellchange](/dom/Event/cellchange)
:

[change](/dom/Event/change)
:

[contextmenu](/dom/Event/contextmenu)
:

[controlselect](/dom/Event/controlselect)
:

[copy](/dom/Event/copy)
:

[cut](/dom/Event/cut)
:   Fires after a data selection is cut to the clipboard.

[dataavailable](/dom/Event/dataavailable)
:   Fires when new data at a data source becomes available.

[datasetchanged](/dom/Event/datasetchanged)
:   Fires when content at a data source has changed.

[datasetcomplete](/dom/Event/datasetcomplete)
:   Fires when data transfer from the data source has completed.

[deactivate](/dom/Event/deactivate)
:   Sets an active version of an object to not active.

[error](/dom/Event/error)
:   Fires when an error occurs.

[errorupdate](/dom/Event/errorupdate)
:   Executes any error handling associated with the event.

[filterchange](/dom/Event/filterchange)
:

[finish](/dom/Event/finish)
:

## Examples

This example uses [addEventListener](/dom/EventTarget/addEventListener) to listen to the **load** event in order to change the title of the page to indicate that the page is done loading. It uses [isTrusted](/dom/Event/isTrusted) to make sure the event was triggered by the user agent itself and not by some script.

``` js
function initialize(e) {
  if (e.isTrusted) {
    document.title = "The page is done loading.";
  }
}
window.addEventListener("load", initialize, false);
```

This example uses [addEventListener](/dom/EventTarget/addEventListener) to listen to the **keydown** event and suppress key down operations using the [preventDefault](/dom/Event/preventDefault) method of the Event instance object. This causes any key presses that occurs within text fields not to emit text into the fields.

``` js
function suppressPresses(e) {
  e.preventDefault();
}
document.addEventListener("keydown", suppressPresses, false);
```

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## See also

### Related pages

-   BeforeUnloadEvent[BeforeUnloadEvent](/dom/BeforeUnloadEvent)
-   CompositionEvent[CompositionEvent](/dom/CompositionEvent)
-   CustomEvent[CustomEvent](/dom/CustomEvent)
-   DragEvent[DragEvent](/dom/DragEvent)
-   FocusEvent[FocusEvent](/dom/FocusEvent)
-   KeyboardEvent[KeyboardEvent](/dom/KeyboardEvent)
-   MessageEvent[MessageEvent](/dom/MessageEvent)
-   MouseEvent[MouseEvent](/dom/MouseEvent)
-   MouseWheelEvent[MouseWheelEvent](/w/index.php?title=dom/MouseWheelEvent&action=edit&redlink=1)
-   MutationEvent[MutationEvent](/dom/MutationEvent)
-   StorageEvent[StorageEvent](/dom/StorageEvent)
-   TextEvent[TextEvent](/dom/TextEvent)
-   UIEvent[UIEvent](/dom/UIEvent)
-   WheelEvent[WheelEvent](/dom/WheelEvent)
