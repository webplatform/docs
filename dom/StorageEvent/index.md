---
title: 'StorageEvent'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[StorageEvent](https://developer.mozilla.org/en-US/docs/Web/API/StorageEvent) Article]'
  - 'Microsoft Developer Network: [[StorageEvent](http://msdn.microsoft.com/en-us/library/ie/ff974349(v=vs.85).aspx) Article]'
notes:
  - "Missing initStorageEvent\nsee http://msdn.microsoft.com/en-us/library/ie/ff974349(v=vs.85).aspx"
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: Event
    href: /dom/Event
standardization_status: 'W3C Working Draft'
summary: 'Provides event properties that are specific to the onstorage event.'
tags:
  - API
  - Objects
  - DOM
uri: dom/StorageEvent

---
## Summary

Provides event properties that are specific to the onstorage event.

Inherits from [Event](/dom/Event)[Event](/dom/Event)

## Properties

*No properties.*

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

## Examples

The following code example demonstrates how to respond to storage events.

``` js
function reportStorage(evt) {
    alert("Storage was updated for " + evt.url);
}
window.onload = function() {
if(window.sessionStorage){
    window.addEventListener('storage',reportStorage,false);
    window.sessionStorage.setItem('key','value');
}
}
```

## Usage

     Used to notify a user that data has been successfully written to their DOM Storage area of their device.

## Notes

In MSIE/Windows browsers...

1. DOM storage is user and/or administrator configurable from Internet Options and Group Policy and can be enabled/disabled in the client browser.

2. For local (x)html files that use the file: protocol, sessionStorage and localStorage are undefined.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 5.11.1.5
