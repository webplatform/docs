---
title: 'location'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary, examples, compatibility, standards, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/KeyboardEvent
    href: /dom/KeyboardEvent
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/KeyboardEvent/location

---
Property of [dom/KeyboardEvent](/dom/KeyboardEvent)[dom/KeyboardEvent](/dom/KeyboardEvent)

## Syntax

``` js
var result = element.location;
element.location = value;
```

## Notes

### Remarks

The **location** property is not set during [**onkeypress**](/dom/KeyboardEvent/keypress) events. It is available only during [**onkeydown**](/dom/KeyboardEvent/keydown) and [**onkeyup**](/dom/KeyboardEvent/keyup) events.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Events Specification](http://go.microsoft.com/fwlink/p/?linkid=203756), Section 5.2.6
