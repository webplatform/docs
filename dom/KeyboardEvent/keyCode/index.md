---
title: 'keyCode'
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
  - API
  - Object
  - Properties
  - DOM
uri: dom/KeyboardEvent/keyCode

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/KeyboardEvent](/dom/KeyboardEvent)[dom/KeyboardEvent](/dom/KeyboardEvent)

## Syntax

``` js
var result = element.keyCode;
element.keyCode = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **keyCode** property represents the character code during the [**onkeypress**](/dom/KeyboardEvent/keypress) event and the unmodified scan code of the key during [**onkeydown**](/dom/KeyboardEvent/keydown) and [**onkeyup**](/dom/KeyboardEvent/keyup) events. To detect whether the Alt, Ctrl, Meta, or Shift key is also pressed, see the [**altKey**](/dom/KeyboardEvent/altKey), [**ctrlKey**](/dom/KeyboardEvent/ctrlKey), [**metaKey**](/dom/KeyboardEvent/metaKey), or [**shiftKey**](/dom/KeyboardEvent/shiftKey) property of the event. The **keyCode** property is provided for compatibility only. The latest version of the Document Object Model (DOM) Events specification defines a [**key**](/dom/KeyboardEvent/key) property instead.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Events Specification](http://go.microsoft.com/fwlink/p/?linkid=203756), Section 5.2.6
