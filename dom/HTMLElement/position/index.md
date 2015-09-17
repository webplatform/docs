---
title: 'position'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'stub MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
standardization_status: Unknown
tags:
  - API_Object_Properties
  - DOM
uri: dom/HTMLElement/position

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.position;
element.position = value;
```

## Notes

### Remarks

When the [**value**](/html/attributes/value_(HTMLProgressElement)) attribute is omitted from a [**progress**](/html/elements/progress) element, the element is indeterminate. The **progress** element shows activity, but not how much progress has actually been made. If the [**value**](/html/attributes/value_(HTMLProgressElement)) attribute is used without a [**max**](/html/attributes/max(HTMLProgressElement)) value, the range is from 0 to 1. The following example displays the current value of the **position** property when the progress bar is changed.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.16

## See also

### Related pages

-   HTMLProgressElement[HTMLProgressElement](/html/elements/progress)
