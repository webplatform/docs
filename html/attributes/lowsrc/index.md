---
title: 'lowsrc'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: lowsrc
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: 'Allows authors to specify a lower resolution image to be shown while the actual image is downloading.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/lowsrc

---
## Summary

Allows authors to specify a lower resolution image to be shown while the actual image is downloading.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

If the [**src**](/html/attributes/src) property is set in code, the new URL starts loading into the image area and aborts the transfer of any image data that is already loading into the same area. If you want to alter the **lowsrc** property, you must do so before setting the **src** property. If the URL in the **src** property references an image that is not the same size as the image cell it is loaded into, the source image is scaled to fit.

### Syntax

## See also

### Related pages

-   `img`
-   `input`
-   `input type=image`
