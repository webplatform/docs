---
title: 'createEvent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: Deprecated
summary: 'Creates a DOM event of the specified type. This method is deprecated; use event constructors (CustomEvent) instead.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Document/createEvent

---
## Summary

Creates a DOM event of the specified type. This method is deprecated; use event constructors (CustomEvent) instead.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var event = document.createEvent(eventType);
```

## Parameters

### eventType

 Data-type
:   String

 One of the following values. Case is not important.

## Return Value

Returns an object of type DOM NodeDOM Node

The created event.

## Examples

The following example demonstrates how to create and dispatch a custom event that bubbles and cannot be canceled.

``` js
var evt = document.createEvent("Event");
evt.initEvent("custom", true, false);
document.getElementById('target').dispatchEvent(evt);
```

To respond to the custom event created previously, the following example adds an event handler that interacts with the event by setting a expando property named `detail`.

``` js
function reportEvent(evt) {
    evt.detail = "Success.";
}
var p = document.getElementById('target');
p.addEventListener("custom", reportEvent, false);
```

## Notes

If the event object is to be dispatched with [**dispatchEvent**](/dom/EventTarget/dispatchEvent), the appropriate event initialization method must be called. For example, after creating an event of type **UIEvent**, call [**initUIEvent**](/dom/UIEvent/initUIEvent) to initialize the event object's values. **Security Warning:  **For security reasons, events generated with **createEvent** are untrusted and have a [**isTrusted**](/dom/Event/isTrusted) value of false.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/#widl-DocumentEvent-createEvent)
:   Working Draft
