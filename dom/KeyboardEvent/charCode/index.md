---
title: 'charCode'
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
uri: dom/KeyboardEvent/charCode

---
Property of [dom/KeyboardEvent](/dom/KeyboardEvent)[dom/KeyboardEvent](/dom/KeyboardEvent)

## Syntax

``` js
var result = element.charCode;
element.charCode = value;
```

## Notes

### Remarks

The **charCode** property represents the character code during the [**onkeypress**](/dom/KeyboardEvent/keypress) event and the unmodified scan code of the key during [**onkeydown**](/dom/KeyboardEvent/keydown) and [**onkeyup**](/dom/KeyboardEvent/keyup) events. To detect whether the Alt, Ctrl, Meta, or Shift key is also pressed, see the [**altKey**](/dom/KeyboardEvent/altKey), [**ctrlKey**](/dom/KeyboardEvent/ctrlKey), [**metaKey**](/dom/KeyboardEvent/metaKey), or [**shiftKey**](/dom/KeyboardEvent/shiftKey) property of the event. The **charCode** property is provided for compatibility only. The latest version of the Document Object Model (DOM) Events specification defines a [**key**](/dom/KeyboardEvent/key) property instead.

### Syntax

### Standards information

There are no standards that apply here.
