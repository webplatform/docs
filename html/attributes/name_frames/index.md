---
title: name (frames)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: 'html/attributes/name (frames)'

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
## <span>Examples</span>

This example uses scripting to set the **name** property of a frame.

``` html
parent.frames[0].name="Left";
```

This example shows how the **NAME** attribute for a window can be persisted in HTML, but only when defined in a frame within a frameset.

``` html
<FRAMESET>
    <FRAME NAME="Left" SRC="blank.htm">
    <FRAME NAME="Right" SRC="contents.htm">
</FRAMESET>
```

## <span>Notes</span>

### <span>Remarks</span>

The **name** property identifies which frame displays the content of a linked document.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `frame`
-   `frameSet`
-   `iframe`
