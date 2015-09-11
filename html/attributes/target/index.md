---
title: target
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Target is a link attribute, which defines where to open the link.'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/open
uri: html/attributes/target

---
## <span>Summary</span>

Target is a link attribute, which defines where to open the link.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
<http://docs.webplatform.org/wiki/html/elements/a>

</td>
</tr>
</table>
**Target** is a link attribute that defines in what window a link will open.

## <span>Examples</span>

A target value of "\_blank" will cause the page to open in a new window.

``` html


<a href="#" target="_blank">Link Text</a>
```

</pre>

A target value of "\_self" will cause the page to open in the same window or frame.

``` html


<a href="#" target="_self">Link Text</a>
```

</pre>

A target value of "\_parent" will cause the page to open in parent frame of the element.

``` html


<a href="#" target="_parent">Link Text</a>
```

</pre>

A target value of "\_top" will cause the page to open in the top-most frame.

``` html


<a href="#" target="_top">Link Text</a>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

The window **name** is an optional argument in the [**open**](/w/index.php?title=dom/methods/open&action=edit&redlink=1) scripting method. If there is no existing window or frame with the same **name** as specified in the **target**, a new window is opened with a **name** equal to the value of the **target**.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `a`
-   `area`
-   `base`
-   `form`
-   `link`
