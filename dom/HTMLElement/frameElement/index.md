---
title: frameElement
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples best practices, compatibility, standards, clean-up of MSDN sections'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
standardization_status: Unknown
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/frameElement

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.frameElement;
element.frameElement = value;
```

## Examples

The following example retrieves the **frame** element of the window and sets its source URL to Microsoft Developer Network (MSDN) Online.

``` html
<SCRIPT LANGUAGE="JScript">
    var oFrame = window.frameElement;
    oFrame.src = "http://msdn.microsoft.com";
</SCRIPT>
```

## Notes

### Remarks

The window must be a **frame** or **iframe**.

### Syntax

## See also

### Related pages (MSDN)

-   `window`
