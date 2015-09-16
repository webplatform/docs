---
title: 'marginWidth'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: marginWidth
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the left and right margin widths before displaying the text in a frame.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/marginWidth

---
## Summary

Sets or retrieves the left and right margin widths before displaying the text in a frame.

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

Margins cannot be less than 1 pixel or so large that the text cannot be displayed. If **marginWidth** is specified but [**marginHeight**](/html/attributes/marginHeight) is not, **marginHeight** is set to 0. If the document hosted in the **frame** or **iframe** has [**margin-left**](/css/properties/margin-left) or [**margin-right**](/css/properties/margin-right) properties set either through Cascading Style Sheets (CSS) or through the [**leftMargin**](/html/attributes/leftMargin) or [**rightMargin**](/html/attributes/rightMargin) properties of the **body** element, then this property is ignored.

### Syntax

## See also

### Related pages

-   `frame`
-   `iframe`
-   `LayoutRect`
-   marginHeight[marginHeight](/html/attributes/marginHeight)
