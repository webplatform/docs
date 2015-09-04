---
title: clientHeight
tags:
  - API
  - Object
  - Properties
  - DOM
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientHeight.htm'
uri: dom/HTMLElement/clientHeight

---
# clientHeight

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.clientHeight;
element.clientHeight = value;
```

## Examples

This example shows how the **clientHeight** property and the [**offsetHeight**](/dom/HTMLElement/offsetHeight) property measure document height differently. The height of the **div** is set to 100, and this is the value retrieved by the **offsetHeight** property, not the **clientHeight** property.

    <div id="oDiv" style="overflow: scroll; width: 200px; height: 100px">
        . . . </div>
    <button onclick="alert(oDiv.clientHeight)">client height</button>
    <button onclick="alert(oDiv.offsetHeight)">offset heightY</button>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientHeight.htm)

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

