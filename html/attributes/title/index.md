---
title: title
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/title_1.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/title

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

This example uses the **title** property to display advisory text when the user hovers the mouse pointer over the text.

``` html
<SCRIPT>
function boldAdvise(src) {
    src.title="this is bold text";
    return;
    }
</SCRIPT>
:
<SPAN onmouseover="boldAdvise(this)">bold section</SPAN>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/title_1.htm)

## Notes

### Remarks

Windows Internet Explorer renders the title as a ToolTip when the user hovers the mouse over the object. Titles are limited to 512 total characters; this limit includes control characters, such as line feeds, carriage returns, and so on. In Windows CE, ToolTips do not appear when a user hovers the mouse pointer over objects. Renders the title as a ToolTip when the user hovers a mouse or finger over objects Titles are limited to 512 total characters; this limit includes control characters, such as line feeds, carriage returns, and so on.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 7.4.3

## See also

### Related pages

-   `a`
-   `abbr`
-   `acronym`
-   `address`
-   `applet`
-   `area`
-   `article`
-   `aside`
-   `b`
-   `bdo`
-   `big`
-   `blockQuote`
-   `body`
-   `br`
-   `button`
-   `caption`
-   `center`
-   `cite`
-   `code`
-   `col`
-   `colGroup`
-   `custom`
-   `dd`
-   `del`
-   `dfn`
-   `dir`
-   `div`
-   `dl`
-   `dt`
-   `em`
-   `embed`
-   `fieldSet`
-   `figcaption`
-   `figure`
-   `font`
-   `footer`
-   `form`
-   `frame`
-   `frameSet`
-   `head`
-   `header`
-   `hgroup`
-   `hn`
-   `hr`
-   `html`
-   `i`
-   `iframe`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
-   `input type=hidden`
-   `input type=image`
-   `input type=password`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=text`
-   `ins`
-   `isIndex`
-   `kbd`
-   `label`
-   `legend`
-   `li`
-   `listing`
-   `map`
-   `mark`
-   `marquee`
-   `menu`
-   `nav`
-   `nextID`
-   `noBR`
-   `object`
-   `ol`
-   `optGroup`
-   `option`
-   `p`
-   `plainText`
-   `pre`
-   `q`
-   `rt`
-   `ruby`
-   `s`
-   `samp`
-   `section`
-   `select`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `sub`
-   `sup`
-   `table`
-   `tBody`
-   `td`
-   `textArea`
-   `tFoot`
-   `th`
-   `tHead`
-   `tr`
-   `tt`
-   `u`
-   `ul`
-   `var`
-   `xmp`
-   `title`
