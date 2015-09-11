---
title: FocusEvent
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: UIEvent
    href: /dom/UIEvent
tags:
  - API
  - Objects
  - DOM
uri: dom/FocusEvent

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Inherits from [UIEvent](/dom/UIEvent)[UIEvent](/dom/UIEvent)

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

API Name
:   Summary

[initFocusEvent](/dom/FocusEvent/initFocusEvent)
:   Initializes a new **FocusEvent** that the [createEvent](/dom/Document/createEvent) method created.

## <span>Events</span>

API Name
:   Summary

[blur](/dom/FocusEvent/blur)
:

[focus](/dom/FocusEvent/focus)
:

[focusin](/dom/FocusEvent/focusin)
:

[focusout](/dom/FocusEvent/focusout)
:

## <span>Inherited from UIEvent</span>

### <span>Properties</span>

API Name
:   Summary

[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.

[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

### <span>Methods</span>

API Name
:   Summary

[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

### <span>Events</span>

API Name
:   Summary

[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.

[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

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
