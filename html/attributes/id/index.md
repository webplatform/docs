---
title: id
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/id.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The id attribute is used for identifying elements in a document.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/id

---
## Summary

The id attribute is used for identifying elements in a document.

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

This example gets the **ID** attribute of each cell of a table. When the user clicks a cell, the object of the cell is passed to a function which returns the object's ID.

``` html
<script>
function getID(oObject)
{
    var id = oObject.id;
    alert("This object's ID attribute is set to \"" + id + "\".");
}
</script>
<table border="">
    <tr>
        <td id="firstCell" onclick="getID(this);">Table Cell 1</td>
        <td id="secondCell" onclick="getID(this);">Table Cell 2</td>
        <td id="thirdCell" onclick="getID(this);">Table Cell 3</td>
    </tr>
</table>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/id.htm)

## Notes

### Remarks

The **id** is an SGML identifier used as the target for hypertext links or for naming particular objects in associated style sheets. The **id** should be unique throughout the scope of the current document. If a document contains more than one object with the same identifier, the objects are exposed as a collection that can be referenced only in ordinal position. In versions earlier than Microsoft Internet Explorer 5, this property is read-only.

### Syntax

## See also

### Related pages

-   `style`
-   `a`
-   `abbr`
-   `acronym`
-   `address`
-   `applet`
-   `area`
-   `b`
-   `base`
-   `baseFont`
-   `bdo`
-   `bgSound`
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
-   `comment`
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
-   `font`
-   `form`
-   `frame`
-   `frameSet`
-   `head`
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
-   `link`
-   `listing`
-   `map`
-   `marquee`
-   `menu`
-   `nextID`
-   `noBR`
-   `noFrames`
-   `noScript`
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
-   `script`
-   `select`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `styleSheet`
-   `sub`
-   `sup`
-   `table`
-   `tBody`
-   `td`
-   `textArea`
-   `tFoot`
-   `th`
-   `tHead`
-   `title`
-   `tr`
-   `tt`
-   `u`
-   `ul`
-   `var`
-   `wbr`
-   `xml`
-   `xmp`
