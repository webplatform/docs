---
title: MutationEvent
tags:
  - API
  - Objects
  - DOM
  - DOMEvents
readiness: 'Ready to Use'
standardization_status: Deprecated
summary: "Represents events for tracking modifications, insertions and deletions of attributes and nodes in the DOM.\nMutation Events (W3C DOM Level 3 Events) have been deprecated in favor of Mutation Observers (W3C DOM4).\n"
uri: dom/MutationEvent

---
# MutationEvent

## Summary

Represents events for tracking modifications, insertions and deletions of attributes and nodes in the DOM. Mutation Events (W3C DOM Level 3 Events) have been deprecated in favor of Mutation Observers (W3C DOM4).

Do not use it in old or new projects.

Pages or Web apps using it may break at any time.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[Event](/dom/Event)</span></span>

## Properties

API Name
:   Summary
[attrChange](/dom/MutationEvent/attrChange)
:   Gets a value that indicates what type of change occurred.
[attrName](/dom/MutationEvent/attrName)
:   Gets the name of the attribute that changed.
[newValue](/dom/MutationEvent/newValue)
:   Gets the new value of the attribute or text node.
[prevValue](/dom/MutationEvent/prevValue)
:   Gets the previous value of the attribute or text node.
[relatedNode](/dom/MutationEvent/relatedNode)
:   Gets a second node related to a mutation event.

## Methods

API Name
:   Summary
[initMutationEvent](/dom/MutationEvent/initMutationEvent)
:   Initializes a new DOM mutation (modification) event that the [**createEvent**](/dom/Document/createEvent) method created.

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
[beforedeactivate](/dom/Event/beforedeactivate)
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

**Needs Examples**: This section should include examples.

## Notes

Mutation events occur when DOM nodes are inserted and removed, or when character data or attributes are modified. For more information, see [**initMutationEvent**](/dom/MutationEvent/initMutationEvent).

## Related specifications

Specification
:   Status
[DOM Level 2 Events](http://www.w3.org/TR/DOM-Level-2-Events/)
:   Recommendation

## See also

### Related articles

#### Deprecated

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   **MutationEvent**

-   [attrChange](/dom/MutationEvent/attrChange)

-   [attrName](/dom/MutationEvent/attrName)

-   [initMutationEvent](/dom/MutationEvent/initMutationEvent)

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   [relatedNode](/dom/MutationEvent/relatedNode)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   [unescape](/javascript/unescape)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[MutationEvent](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Mutation_events) Article]

Portions of this content come from the Microsoft Developer Network: [[MutationEvent](http://msdn.microsoft.com/en-us/library/ie/ff974346(v=vs.85).aspx) Article]

Portions of this content come from HTML5Rocks! [[MutationEvent samples](http://www.html5rocks.com/en/search?q=MutationEvent) article]

