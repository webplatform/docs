---
title: ol – ordered list
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/eb2b4134dc595b6dbf17'
  - 'http://gist.github.com/3386252885e8db151a1f'
notes:
  - 'Correct Title format. Add Category information. Complete Compatibility table.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLOListElement](/dom/HTMLOListElement)'
readiness: 'In Progress'
summary: 'The ol element is used to define an ordered list. The element encloses one or more list items, enclosed in li elements.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/concepts/flowContent
uri: html/elements/ol

---
## ol

For technical reasons, the title of this article is not the text used to call this API. Instead, use `ol`

## Summary

The ol element is used to define an ordered list. The element encloses one or more list items, enclosed in li elements.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLOListElement](/dom/HTMLOListElement)

<table class="wikitable">
<tr>
<th style="vertical-align: top" id="permitted-contents">
Permitted contents

</th>
<td style="vertical-align: top; padding-top: 10px">
One of the following:

-   Either: Zero or more [**li**](/html/elements/li) elements.
-   Or: A [**template**](/html/elements/template) element.
-   Or: any combination of the above two

</td>
</tr>
<tr>
<th id="permitted-parents">
Permitted parents

</th>
<td>
Any element that can contain [flow content](/w/index.php?title=html/concepts/flowContent&action=edit&redlink=1).

</td>
</tr>
<tr>
<th id="tag-omission">
Tag omission

</th>
<td>
A **ol** element must have both a start tag and an end tag.

</td>
</tr>
</table>
The **ordered list**, represented by the **ol** element, is most often used to group a list of items, enclosed in [**li**](/html/elements/li) elements, together in an ordered and semantic way.

## Examples

This example uses the **ol** element to create a numbered list.

``` html
<ol>
  <li>This is the first list item</li>
  <li>This is the second list item</li>
</ol>
```

[View live example](http://code.webplatform.org/gist/eb2b4134dc595b6dbf17)

The **ol** element with the **type** attribute set to **a**.

``` html
<ol type="a">
  <li>This is the first list item</li>
  <li>This is the second list item</li>
</ol>
```

[View live example](http://code.webplatform.org/gist/3386252885e8db151a1f)

Typical browser default CSS properties for the **ol** element.

``` css
display: block;
list-style-type: decimal;
margin-top: 16px;
margin-bottom: 16px;
```

## Notes

### Remarks

The [**type**](/html/attributes/type_(ul,li,ol_elements)) attribute sets the list type for all ensuing lists unless a different type value is set.

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 10.2

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-ol-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-ol-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/lists.html#edef-OL)
:   W3C Recommendation

## See also

### Other articles

-   [`dir`](/html/elements/dir)
-   [`menu`](/html/elements/menu)
-   [`ul`](/html/elements/ul)
-   [`li`](/html/elements/li)
-   [`dl`](/html/elements/dl)
-   [`dt`](/html/elements/dt)
-   [`dd`](/html/elements/dd)
