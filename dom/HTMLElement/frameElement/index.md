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

## <span>Syntax</span>

``` js
var result = element.frameElement;
element.frameElement = value;
```

## <span>Examples</span>

The following example retrieves the **frame** element of the window and sets its source URL to Microsoft Developer Network (MSDN) Online.

``` html
<SCRIPT LANGUAGE="JScript">
    var oFrame = window.frameElement;
    oFrame.src = "http://msdn.microsoft.com";
</SCRIPT>
```

## <span>Notes</span>

### <span>Remarks</span>

The window must be a **frame** or **iframe**.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `window`
