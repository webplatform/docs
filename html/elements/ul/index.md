---
title: 'ul – unordered list'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: ul
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLUListElement](/dom/HTMLUListElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The ul element is used to define an unordered list. The element encloses one or more list items, enclosed in li elements.'
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/concepts/flowContent
uri: html/elements/ul

---
## ul

For technical reasons, the title of this article is not the text used to call this API. Instead, use `ul`

## Summary

The ul element is used to define an unordered list. The element encloses one or more list items, enclosed in li elements.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLUListElement](/dom/HTMLUListElement)

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
A **ul** element must have both a start tag and an end tag.

</td>
</tr>
</table>
 The **unordered list**, represented by the **ul** element, is most often used to group a list of items, enclosed in [**li**](/html/elements/li) elements, together in a semantic way. Usually, the order in which the items are presented is not important.

## Examples

This example uses the **ul** element to create a bulleted list.

``` html
<ul>
  <li>Alice</li>
  <li>Bob</li>
  <li>Carol</li>
</ul>
```

Example with nested lists

``` html
<ul>
  <li>Alice <ul>
    <li>Red</li>
    <li>Green</li>
  </ul>
  </li>
  <li>Bob <ul>
    <li>Green</li>
    <li>Cyan</li>
  </ul></li>
  <li>Carol <ul>
    <li>Magenta</li>
    <li>Yellow</li>
  </ul></li>
</ul>
```

Typical browser default CSS properties for the **ul** element.

``` css
display: block;
list-style-type: disc;
margin-top: 16px;
margin-bottom: 16px;
```

## Notes

### Remarks

The [**type**](/html/attributes/type_(ul,li,ol_elements)) attribute sets the list type for all ensuing lists unless a different type value is set. The **ul** element inherits its [**line-height**](/css/properties/line-height) from the height of the [**font**](/css/properties/font) attribute for the **body**. For example, if the [**font-size**](/css/properties/font-size) attribute for the **body** is larger than the **font-size** attribute for the **ul** element, the list items in the **ul** are spaced according to the **font-size** of the **body**.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-ul-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-ul-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/lists.html#edef-UL)
:   W3C Recommendation

## See also

### Other articles

-   [`dir`](/html/elements/dir)
-   [`menu`](/html/elements/menu)
-   [`ol`](/html/elements/ol)
-   [`li`](/html/elements/li)
-   [`dl`](/html/elements/dl)
-   [`dt`](/html/elements/dt)
-   [`dd`](/html/elements/dd)
