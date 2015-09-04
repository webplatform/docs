---
title: keyCode
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Summary, examples, compatibility, standards, clean-up of MSDN import'
uri: dom/KeyboardEvent/keyCode

---
# keyCode

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/KeyboardEvent](/dom/KeyboardEvent)</span></span>

## Syntax

``` {.js}
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

