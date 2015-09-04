---
title: lowsrc
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: Deprecated
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Allows authors to specify a lower resolution image to be shown while the actual image is downloading.'
uri: html/attributes/lowsrc

---
# lowsrc

## Summary

Allows authors to specify a lower resolution image to be shown while the actual image is downloading.

Applies to
:    ?

**Needs Examples**: This section should include examples.

## Notes

### Remarks

If the [**src**](/html/attributes/src) property is set in code, the new URL starts loading into the image area and aborts the transfer of any image data that is already loading into the same area. If you want to alter the **lowsrc** property, you must do so before setting the **src** property. If the URL in the **src** property references an image that is not the same size as the image cell it is loaded into, the source image is scaled to fit.

### Syntax

## See also

### Related pages (MSDN)

-   `img`
-   `input`
-   `input type=image`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

