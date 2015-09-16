---
title: AnimationEvent
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: Event
    href: /dom/Event
summary: 'Provides specific contextual information associated with animation events.'
tags:
  - API
  - Objects
  - DOM
uri: dom/AnimationEvent

---
## Summary

Provides specific contextual information associated with animation events.

Inherits from [Event](/dom/Event)[Event](/dom/Event)

## Properties

API Name
:   Summary

[animationName](/dom/AnimationEvent/animationName)
:   The value of the *animation-name* property of the animation that fired the animation event.

[elapsedTime](/dom/AnimationEvent/elapsedTime)
:   The amount of time the animation has been running, in seconds, since the event fired, excluding any time the animation was paused.

[pseudoElement](/dom/AnimationEvent/pseudoElement)
:   A DOMString, starting with "::", containing the name of the pseudo-element the animation runs on. If the animation runs on the element rather than on a pseudo-element, this property contains an empty string, "".

## Methods

*No methods.*

## Events

*No events.*

## Inherited from Event

### Properties

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

### Methods

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

### Events

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

## Notes

AnimationEvent objects provide information about events that occur related to Cascading Style Sheets (CSS) animations. Several animation related events are available. For example, the start and end of an animation, and the end of each iteration of an animation all generate Document Object Model (DOM) events. An element can have multiple properties being animated simultaneously. This can occur either with a single [**animationName**](/dom/AnimationEvent/animationName) value with keyframes containing multiple properties, or with multiple **animationName** values. For the purposes of events, each **animationName** specifies a single animation. Therefore an event will be generated for each **animationName** value and not necessarily for each property being animated.

The time the animation has been running is sent with each event generated. This allows the event handler to determine the current iteration of a looping animation or the current position of an alternating animation. This time does not include any time the animation was in the paused play state.

The different types of animation events that can occur are:

**animationstart** - The animationstart event occurs at the start of the animation. If there is an animation-delay then this event will fire once the delay period has expired. A negative delay will cause the event to fire with an elapsedTime equal to the absolute value of the delay.

-   Bubbles: Yes
-   Cancelable: No
-   Context Info: animationName, pseudoElement

**animationend** - The animationend event occurs when the animation finishes.

-   Bubbles: Yes
-   Cancelable: No
-   Context Info: animationName, elapsedTime, pseudoElement

**animationiteration** - The animationiteration event occurs at the end of each iteration of an animation, except when an animationend event would fire at the same time. This means that this event does not occur for animations with an iteration count of one or less.

-   Bubbles: Yes
-   Cancelable: No
-   Context Info: animationName, elapsedTime, pseudoElement
