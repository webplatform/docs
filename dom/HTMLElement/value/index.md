---
title: 'value'
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
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/HTMLElement/value

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.value;
element.value = value;
```

## Notes

### Remarks

Windows Internet Explorer 8 or later. In IE8 Standards mode, the **value** property is correctly reported as a canonical attribute name. For example, `<input type="text" readonly>` and `<input type="text" readonly="readonly">` would both set the input text field to read-only. In IE8 mode, the value is evaluated as a canonical value, `"readonly"`. In earlier document compatibility modes, it is evaluated as a Boolean value, true. For more information, see Attribute Differences in Internet Explorer 8. **value** was introduced in Microsoft Internet Explorer 6.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages

-   attributes[attributes](/dom/Node/attributes)
-   nodeValue[nodeValue](/dom/Node/nodeValue)
