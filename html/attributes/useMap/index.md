---
title: useMap
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/useMap

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

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

The following example defines the map. Clicking within the rectangular areas of the map loads a new page into a target window named `frame1`.

``` html
<MAP NAME="map1">
   <AREA NAME="area1" COORDS="4,20,20,40" href="left_arrow.htm" target="frame1"/>
   <AREA NAME="area2" COORDS="116,20,100,40" href="right_arrow.htm" target="frame1"/>
</MAP>
```

The following example shows **USEMAP** with an image.

``` html
<IMG USEMAP="#map1" BORDER="0" SRC="double_pointed_arrow.png">
```

The following example shows **USEMAP** with an **object**. This technique requires Internet Explorer 8 and later.

``` html
<OBJECT data="double_pointed_arrow.png" border="0" type="image/gif" usemap="#map1">
</OBJECT>
```

## Notes

### Remarks

The **useMap** property identifies the image as a client-side image map by associating a **map** object with the image. This **map** object contains **area** objects that define regions within the image. The user can click these regions to navigate to a designated URL. You can dynamically assign the maps to the image through the **useMap** property. In Microsoft Internet Explorer 6 and greater, this property applies to the **object** and **input** objects.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 13.6.1

## See also

### Related pages

-   `img`
-   `object`
-   `input`
