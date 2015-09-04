---
title: CompositionEvent
tags:
  - API
  - Objects
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'An interfact that provides specific contextual information associated with Composition Events.'
uri: dom/CompositionEvent

---
# CompositionEvent

## Summary

An interfact that provides specific contextual information associated with Composition Events.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[UIEvent](/dom/UIEvent)</span></span>

## Properties

API Name
:   Summary
[data](/dom/CompositionEvent/data)
:   Gets the text affected by the composition event.
[locale](/dom/CompositionEvent/locale)
:   Gets the locale name (language code, e.g., "en-US", "fr", "de", "ja", etc.) for the composition event, if available; otherwise, the empty string.

## Methods

*No methods.*

## Events

*No events.*

## Inherited from UIEvent

### Properties

API Name
:   Summary
[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.
[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

### Methods

API Name
:   Summary
[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

### Events

API Name
:   Summary
[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.
[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

