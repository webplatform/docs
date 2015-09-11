---
title: TransitionEvent
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[TransitionEvent](https://developer.mozilla.org/en-US/docs/Web/API/TransitionEvent.TransitionEvent) Article]'
  - 'Microsoft Developer Network: [[TransitionEvent Object](http://msdn.microsoft.com/en-us/library/ie/hh772135(v=vs.85).aspx) Article]'
notes:
  - "Missing Events\ntransitionstart, transitionend\nduplicate propertyName entry in Properties\n\nmissing animationName property."
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: Event
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Provides specific contextual information associated with Cascading Style Sheets (CSS) transitions.'
tags:
  - API
  - Objects
  - DOM
uri: dom/TransitionEvent

---
## <span>Summary</span>

Provides specific contextual information associated with Cascading Style Sheets (CSS) transitions.

Inherits from [Event](/dom/Event)[Event](/dom/Event)

## <span>Properties</span>

API Name
:   Summary

[elapsedTime](/dom/TransitionEvent/elapsedTime)
:   The amount of time the transition has been running, in seconds.

[propertyName](/dom/TransitionEvent/propertyName)
:   Specifies or retrives a string containg the name of the changed property.

## <span>Methods</span>

API Name
:   Summary

[initTransitionEvent](/dom/TransitionEvent/initTransitionEvent)
:   Initializes a transition event created using the deprecated Document.createEvent("TransitionEvent") method.

## <span>Events</span>

*No events.*

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

## <span>Notes</span>

### <span>Remarks</span>

The completion of a CSS transition generates a corresponding Document Object Model (DOM) event. An event is fired for each property that undergoes a transition. This allows a content developer to perform actions that synchronize with the completion of a transition.

Each event provides the name of the property the transition is associated with as well as the duration of the transition.

## <span>Related specifications</span>

[CSS Transitions](http://dev.w3.org/csswg/css-transitions/#Events-TransitionEvent)
:   Working Draft
