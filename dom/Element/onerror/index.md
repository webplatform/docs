---
title: 'onerror'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, and compat'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API_Object_Properties
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/onerror

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.onerror;
element.onerror = value;
```

## Notes

### Remarks

When an error occurs, the current operation is stopped and the error is passed by the [**error**](/dom/Element/error) property. Displays the error message when a problem occurs and executes any error handling routine associated with the event.

### Syntax

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

