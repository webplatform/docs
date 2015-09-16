---
title: 'CompositionEvent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: UIEvent
    href: /dom/UIEvent
standardization_status: 'W3C Working Draft'
summary: 'An interfact that provides specific contextual information associated with Composition Events.'
tags:
  - API
  - Objects
  - DOM
uri: dom/CompositionEvent

---
## Summary

An interfact that provides specific contextual information associated with Composition Events.

Inherits from [UIEvent](/dom/UIEvent)[UIEvent](/dom/UIEvent)

## Properties

API Name
:   Summary

[html/elements/data](/dom/CompositionEvent/data)
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

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
