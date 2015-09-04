---
title: allowTransparency
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; update/improve example; update descriptions'
summary: 'Sets or retrieves whether the object can be transparent.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/allowTransparency.htm'
uri: html/attributes/allowTransparency

---
# allowTransparency

## Summary

Sets or retrieves whether the object can be transparent.

Applies to
:    ?

## Examples

The following example shows four ways to use the **allowTransparency** attribute, with and without the [**background-color**](/css/properties/background-color) attribute. Because the **allowTransparency** attribute of Frame1 is set to **true**, Frame1 renders red, the background color of the parent document. The **allowTransparency** attribute of Frame2 is also set to **true**, however the **background-color** attribute of Frame2 is set to `green`, so Frame2 renders green. Because the **allowTransparency** attribute of Frame3 is set to **false** (the default value), Frame3 renders white, the color of the **t:SRC** document. The **allowTransparency** attribute of Frame4 is also set to **false**, so Frame4 renders white even though the **background-color** attribute of Frame4 is set to `green`.

    <BODY STYLE="background-color: red">
    <IFRAME ID="Frame1" SRC="transparentBody.htm" allowTransparency="true">
    </IFRAME>
    <IFRAME ID="Frame2" SRC="transparentBody.htm" allowTransparency="true"
      STYLE="background-color: green">
    </IFRAME>
    <IFRAME ID="Frame3" SRC="transparentBody.htm">
    </IFRAME>
    <IFRAME ID="Frame4" SRC="transparentBody.htm"
      STYLE="background-color: green">
    </IFRAME>
    </BODY>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/allowTransparency.htm)

## Notes

### Remarks

When the property is set to **VARIANT\_FALSE**, the [**backgroundColor**](/css/properties/background-color) property of the object can only be that of the window. When the property is set to **VARIANT\_TRUE**, the **backgroundColor** property of the object can be set to any value, including the default value of **transparent**.

### Syntax

### Standards information

There are no standards that apply here. Support for this attribute has been dropped in IE9.

## See also

### Related pages (MSDN)

-   `frame`
-   `iframe`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

