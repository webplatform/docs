---
title: UIEvent
tags:
  - API
  - Objects
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Represents a user interface event, like click, blur, etc.'
uri: dom/UIEvent

---
# UIEvent

## Summary

Represents a user interface event, like click, blur, etc.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[Event](/dom/Event)</span></span>

## Properties

API Name
:   Summary
[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.
[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

## Methods

API Name
:   Summary
[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

## Events

API Name
:   Summary
[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.
[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

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

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[UIEvent](https://developer.mozilla.org/en-US/docs/Web/API/UIEvent) Article]

Portions of this content come from the Microsoft Developer Network: [[UIEvent](http://msdn.microsoft.com/en-us/library/ie/ff974351(v=vs.85).aspx) Article]

