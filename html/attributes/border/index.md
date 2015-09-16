---
title: border
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'Specifies the width of the border around an element. Deprecated in HTML4, not supported in HTML5. Use CSS.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/border

---
## Summary

Specifies the width of the border around an element. Deprecated in HTML4, not supported in HTML5. Use CSS.

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
## Examples

``` html
<img src="smiley.gif" alt="Smiley face" border="5">
```

## Notes

### Remarks

Setting a border to `0` or omitting the attribute causes no border to be displayed. Supplying the **BORDER** attribute without a value defaults to a single border. In Microsoft Internet Explorer 6, This property now applies to the **object** object.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 13.7.3 (Deprecated)

## See also

### Related pages (MSDN)

-   `object`
-   `img`
-   `LayoutRect`
-   `table`
-   `Reference`
-   `borderColor`
-   `borderColorDark`
-   `borderColorLight`
-   `hspace`
-   `vspace`
