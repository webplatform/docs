---
title: name (frames)
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
uri: 'html/attributes/name (frames)'

---
# name (frames)

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:    ?

## Examples

This example uses scripting to set the **name** property of a frame.

    parent.frames[0].name="Left";

This example shows how the **NAME** attribute for a window can be persisted in HTML, but only when defined in a frame within a frameset.

    <FRAMESET>
        <FRAME NAME="Left" SRC="blank.htm">
        <FRAME NAME="Right" SRC="contents.htm">
    </FRAMESET>

## Notes

### Remarks

The **name** property identifies which frame displays the content of a linked document.

### Syntax

## See also

### Related pages (MSDN)

-   `frame`
-   `frameSet`
-   `iframe`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

