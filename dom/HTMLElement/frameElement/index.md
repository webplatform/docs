---
title: frameElement
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'summary, examples best practices, compatibility, standards, clean-up of MSDN sections'
uri: dom/HTMLElement/frameElement

---
# frameElement

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.frameElement;
element.frameElement = value;
```

## Examples

The following example retrieves the **frame** element of the window and sets its source URL to Microsoft Developer Network (MSDN) Online.

    <SCRIPT LANGUAGE="JScript">
        var oFrame = window.frameElement;
        oFrame.src = "http://msdn.microsoft.com";
    </SCRIPT>

## Notes

### Remarks

The window must be a **frame** or **iframe**.

### Syntax

## See also

### Related pages (MSDN)

-   `window`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

