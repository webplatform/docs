---
title: 'tabIndex'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tabindex1.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tabindex2.htm'
compatibility:
  feature: tabIndex
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Represents the tab order of an element.'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/blur
    - dom/events/focus
    - dom/events/keydown
    - dom/events/keypress
    - dom/events/keyup
uri: html/attributes/tabIndex

---
## Summary

Represents the tab order of an element.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
</td>
</tr>
</table>
## Examples

This example uses the **tabIndex** property to specify the tab order for three text fields. In addition, the Submit button is removed by specifying a negative value.

``` html
<input type="text" tabindex="1">
<input type="text">
<input type="text" tabindex="2">
<input type="submit" tabindex="-1">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tabindex1.htm)

This example uses the **tabIndex** property to assign a tab order to an unordered list. To cycle through the list's tab order, the user presses the TAB key. Since the list items can have focus, the focus rectangle surrounds each item the user selects.

``` html
<ul>
    <li>Item 1 (no tab)</li>
    <li>Item 2 (no tab)</li>
    <li>Item 3 (no tab)</li>
</ul>
<ul>
    <li tabindex="1">Tab Item 1</li>
    <li tabindex="2">Tab Item 2</li>
    <li tabindex="3">Tab Item 3</li>
    <li tabindex="4">Tab Item 4</li>
    <li tabindex="5">Tab Item 5</li>
</ul>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tabindex2.htm)

## Notes

### Remarks

The **tabIndex** value determines the tab order as follows:

1.  Objects with a positive **tabIndex** are selected in increasing *p* order and in source order to resolve duplicates.
2.  Objects with an **tabIndex** of zero are selected in source order.
3.  Objects with a negative **tabIndex** are omitted from the tabbing order.

An element can have focus if the **tabIndex** property is set to any valid negative or positive integer. The following elements can have focus and are tab stops by default: [**a**](/html/elements/a), **BODY**, **button**, **frame**, **iframe**, **img**, **input**, **isIndex**, **object**, **select**, **textArea**. The following elements can have focus by default but are not tab stops. These elements can be set as tab stops by setting the **tabIndex** property to a positive integer. **applet**, **div**, **frameSet**, **span**, [**table**](/html/elements/table), **td**. Setting the **tHead** and **tFoot** elements to participate in the tab order will not cause the focus rectangle to display when either receives focus. Elements can become part of the accessibility hierarchy if the **TABINDEX** attribute is set as follows:

-   For Microsoft Internet Explorer 5.01 and later, set the **TABINDEX** attribute to any value.
-   For Microsoft Internet Explorer 5, set the **TABINDEX** attribute to a positive value.

For Internet Explorer 5.01 or above, the attribute may be set to any value in the valid range of `-32767` to `32767`. Content of elements with a closing tag can have focus by default, but are not tab stops. As of Internet Explorer 5, you can set the **tabIndex** property to a valid positive integer to force the content to have a tab stop. Elements that receive focus can fire the [**onblur**](/w/index.php?title=dom/events/blur&action=edit&redlink=1) and [**onfocus**](/w/index.php?title=dom/events/focus&action=edit&redlink=1) events as of Microsoft Internet Explorer 4.0, and the [**onkeydown**](/w/index.php?title=dom/events/keydown&action=edit&redlink=1), [**onkeypress**](/w/index.php?title=dom/events/keypress&action=edit&redlink=1), and [**onkeyup**](/w/index.php?title=dom/events/keyup&action=edit&redlink=1) events as of Internet Explorer 5.

### Syntax

## See also

### Related pages

-   a[a](/html/elements/a)
-   `abbr`
-   acronym[acronym](/html/elements/acronym)
-   `address`
-   `applet`
-   `area`
-   `b`
-   `bdo`
-   `big`
-   `blockQuote`
-   `body`
-   `button`
-   `caption`
-   `center`
-   `cite`
-   `custom`
-   `dd`
-   `del`
-   `dfn`
-   `dir`
-   `div`
-   `dl`
-   `dt`
-   `em`
-   `fieldSet`
-   `font`
-   `form`
-   `frame`
-   `frameSet`
-   `hn`
-   `hr`
-   `i`
-   `iframe`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
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
-   `marquee`
-   `menu`
-   `object`
-   `ol`
-   `p`
-   `plainText`
-   `pre`
-   `q`
-   `rt`
-   `ruby`
-   `s`
-   `samp`
-   `select`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `sub`
-   `sup`
-   table[table](/html/elements/table)
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
