---
title: border (frameSet, iframe)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the space between the frames, including the 3-D border.'
tags:
  - Markup
  - Attributes
  - HTML
uri: 'html/attributes/border (frameSet, iframe)'

---
## <span>Summary</span>

Sets or retrieves the space between the frames, including the 3-D border.

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

## <span>Notes</span>

This property applies either to the outer **frameSet** element or to inner **frameSet** elements. When you specify the **border** property of the outermost **frameSet** element, the **border** properties of any inner **frameSet** elements are ignored. When you do not specify the **border** property of the outermost **frameSet** element, the **border** properties of inner **frameSet** elements are not ignored. Setting a border to zero or omitting the attribute causes no border to be displayed. Supplying the border attribute without a value defaults to a single border.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `frameSet`
-   `iframe`
