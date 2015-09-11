---
title: href
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'compatibility, standards, clean-up of MSDN import, neutral/best practices example'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Location
    href: /dom/Location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Location
summary: 'Sets or retrieves the entire URL as a string.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Location/href

---
## <span>Summary</span>

Sets or retrieves the entire URL as a string.

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## <span>Syntax</span>

``` js
var url = location.href;
location.href = url;
```

## <span>Return Value</span>

Returns an object of type StringString

The URL of the document.

## <span>Examples</span>

This example shows a URL list. The user is taken to the URL selected from the options, if the selection is different from the list's default value.

``` html
<select onchange="window.location.href=this.options[this.selectedIndex].value">
<option value="http://www.microsoft.com/ie">Internet Explorer</option>
<option value="http://www.microsoft.com">Microsoft Home</option>
<option value="http://msdn.microsoft.com">Developer Network</option>
</select>
```

