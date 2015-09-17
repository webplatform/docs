---
title: 'name (window)'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'name (window)'
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/open
uri: 'html/attributes/name (window)'

---
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

This example assigns the **name** property to the window object.

``` html
window.name="MyWindow";
```

This example uses the window's [**open**](/w/index.php?title=dom/methods/open&action=edit&redlink=1) method to assign the **name** property.

``` html
window.open("file.htm","Frame1");
```

## Notes

### Remarks

To access a window's **name** property, use the **window** keyword.

### Syntax

## See also

### Related pages

-   `window`
