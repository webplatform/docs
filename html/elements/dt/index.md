---
title: 'dt – description list topic'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5821157'
compatibility:
  feature: dt
  topic: html
notes:
  - 'Add Category and Compatibility information. Modify/Complete Parent and Children information.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: "The dt element indicates a definition term within a definition list (dl). \n"
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/concepts/flowContent
    - html/concepts/sectioningContent
    - html/concepts/headingContent
uri: html/elements/dt

---
## dt

For technical reasons, the title of this article is not the text used to call this API. Instead, use `dt`

## Summary

The dt element indicates a definition term within a definition list (dl).

A ****dt**** (topic) is usually followed by one or more [**dd**](/html/elements/dd) (definition) elements. Several consecutive ****dt**** are attributed to the [**dd**](/html/elements/dd) element that immediately follows the group.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

<table class="wikitable">
<tr>
<th style="vertical-align: top" id="permitted-contents">
Permitted contents

</th>
<td style="vertical-align: top; padding-top: 10px">
[flow content](/w/index.php?title=html/concepts/flowContent&action=edit&redlink=1), but with no [header](/html/elements/header), [footer](/html/elements/footer), [sectioning content](/w/index.php?title=html/concepts/sectioningContent&action=edit&redlink=1), or [heading content](/w/index.php?title=html/concepts/headingContent&action=edit&redlink=1) descendants.

</td>
</tr>
<tr>
<th id="permitted-parents">
Permitted parents

</th>
<td>
[dl](/html/elements/dl).

</td>
</tr>
</table>
## Examples

The example shows a simple definition list with two item/description pairs.

``` html
<dl>
  <dt>Coffee</dt>
  <dd>A popular hot drink.</dd>
  <dt>Coca Cola</dt>
  <dd>One of the leading brands of a popular cold fizzy drink.</dd>
</dl>
```

[View live example](http://gist.github.com/5821157)

The example shows a definition list with a single item but multiple descriptions for that item.

``` html
<dl>
  <dt>Coffee</dt>
  <dd>A popular hot drink.</dd>
  <dd>A mid brown colour</dd>
  <dd>A common social invitation</dd>
</dl>
```

[View live example](http://gist.github.com/5821157)

The example shows a definition list with a single description and multiple items fitting that description.

``` html
<dl>
  <dt>Coffee</dt>
  <dt>Tea</dt>
  <dt>Vimto (in the North of England)</dt>
  <dd>A popular hot drink.</dd>
</dl>
```

[View live example](http://gist.github.com/5821157)

Typical browser default CSS properties for the **dt** element.

``` css
display: block;
```

## Notes

The **dt** element itself, when used in a [dl](/html/elements/dl) element, does not indicate that its contents are a term being defined, but this can be indicated using the [dfn](/html/elements/dfn) element.

While [HTMLDTElement](/dom/HTMLDTElement) is the defined DOM interface for this element, most browsers currently use [HTMLElement](/dom/HTMLElement) instead.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-dt-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-dt-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/lists.html#edef-DT)
:   W3C Recommendation

## See also

### Other articles

-   [`dd`](/html/elements/dd)
-   [`dl`](/html/elements/dl)

### External resources

-   [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/HTML/Element/dt)
-   [Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/ms535243%28v=vs.85%29.aspx)
