---
title: 'cols (frameSet)'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'cols (frameSet)'
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the number of columns in the table.'
tags:
  - Markup_Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'dom/properties/rows (frameSet, cols)'
uri: 'html/attributes/cols (frameSet)'

---
## Summary

Sets or retrieves the number of columns in the table.

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

This example defines a two-column frame, with the first occupying 40 percent of the available width and the second occupying the remaining 60 percent.

``` html
<FRAMESET COLS="40%, 60%">
```

This example defines a four-column frame. The first is 50 pixels wide, and the fourth is 80 pixels wide. The second occupies two-thirds of the remaining width, while the third occupies the final third of the remaining width.

``` html
<FRAMESET COLS="50, 2*, *, 80">
```

## Notes

### Remarks

The number of comma-separated items is equal to the number of frames contained within the **frameSet**, while the value of each item determines the frame width.

### Syntax

## See also

### Related pages

-   `frameSet`
-   rows[rows](/w/index.php?title=dom/properties/rows_(frameSet,_cols)&action=edit&redlink=1)
