---
title: PopStateEvent
attributions:
  - 'Microsoft Developer Network: [[PopStateEvent](http://msdn.microsoft.com/en-us/library/ie/hh772349(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: Event
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Fires when a history entry changes.'
tags:
  - API
  - Objects
  - DOM
uri: dom/PopStateEvent

---
## <span>Summary</span>

Fires when a history entry changes.

Inherits from [Event](/dom/Event)[Event](/dom/Event)

## <span>Properties</span>

API Name
:   Summary

[state](/dom/PopStateEvent/state)
:   The current history entry's state object (if any).

## <span>Methods</span>

API Name
:   Summary

[initPopStateEvent](/dom/PopStateEvent/initPopStateEvent)
:   Initializes the properties of a PopStateEvent.

## <span>Events</span>

API Name
:   Summary

[popstate](/dom/PopStateEvent/popstate)
:   An event handler that is fired when changes are made to the active history. Calls to pushState or replaceState can trigger this event.

## <span>Inherited from Event</span>

### <span>Properties</span>

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

### <span>Methods</span>

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

### <span>Events</span>

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

## <span>Examples</span>

``` js
window.onpopstate = function(evt) { document.write("location: " + document.location + ", state: " + JSON.stringify(evt.state)); };
```

## <span>Usage</span>

     Used, for example to prevent back navigation to a login page after the user has already logged in.

## <span>Notes</span>

### <span>Remarks</span>

A pop state event is dispatched to the window object every time the active history entry changes. To read the current history entry immediately, invoke `history.state`.

## <span>Related specifications</span>

[The History Interface](http://www.w3.org/TR/html5/browsers.html#the-history-interface)
:   Recommendation
