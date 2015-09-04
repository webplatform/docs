---
title: href
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'compatibility, standards, clean-up of MSDN import, neutral/best practices example'
summary: 'Sets or retrieves the entire URL as a string.'
uri: dom/Location/href

---
# href

## Summary

Sets or retrieves the entire URL as a string.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Location](/dom/Location)</span></span>

## Syntax

``` {.js}
var url = location.href;
location.href = url;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The URL of the document.

## Examples

This example shows a URL list. The user is taken to the URL selected from the options, if the selection is different from the list's default value.

``` {.html}
<select onchange="window.location.href=this.options[this.selectedIndex].value">
<option value="http://www.microsoft.com/ie">Internet Explorer</option>
<option value="http://www.microsoft.com">Microsoft Home</option>
<option value="http://msdn.microsoft.com">Developer Network</option>
</select>
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

