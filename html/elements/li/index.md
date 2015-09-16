---
title: li – list item
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add Compatibility'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLLIElement](/dom/HTMLLIElement)'
readiness: 'In Progress'
summary: 'The li element represents one list item.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/li

---
## Summary

The li element represents one list item.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLLIElement](/dom/HTMLLIElement)

Its parent element may be [ol](/html/elements/ol), [ul](/html/elements/ul), or [menu](/html/elements/menu).

## HTML Attributes

-   `value` = valid integer
    Specifies the ordinal value of the list item.
    The value attribute can be used when the parent element in only a ol element. [[Example B]](#Example_B)

## Examples

This example uses the **li** element to create individual items in an unordered list.

``` html
<ul>
     <li>Art</li>
     <li>History</li>
     <li>Literature</li>
     <li>Sports</li>
     <li>Entertainment</li>
     <li>Science</li>
</ul>
```

This example uses the **li** element to create individual items in an ordered list.

``` html
<ol>
     <li>First</li>
     <li>Second</li>
     <li>Third</li>
</ol>
```

Typical browser default CSS properties for the **li** element.

``` css
display: list-item;
margin-left: 40px;
```

## Notes

### Remarks

The [**type**](/html/attributes/type_(ul,li,ol_elements)) attribute values **disc**, **circle**, and **square** apply to unordered lists; the values **1**, **a**, **A**, **i**, and **I** apply to ordered lists. When the **li** element is absolutely positioned with CSS, the list item marker is not rendered. The default value of the [**display**](/css/properties/display) property for this element is **list-item**.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-li-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-li-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/lists.html#edef-LI)
:   W3C Recommendation

## See also

### Other articles

-   [`dir`](/html/elements/dir)
-   [`menu`](/html/elements/menu)
-   [`ol`](/html/elements/ol)
-   [`ul`](/html/elements/ul)
-   [`dd`](/html/elements/dd)
-   [`dt`](/html/elements/dt)
