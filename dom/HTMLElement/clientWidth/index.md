---
title: clientWidth
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'summary, examples best practices, compatibility, standards, clean-up of MSDN sections'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientWidth.htm'
uri: dom/HTMLElement/clientWidth

---
# clientWidth

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.clientWidth;
element.clientWidth = value;
```

## Examples

This example shows how the **clientWidth** property and the [**offsetWidth**](/dom/HTMLElement/offsetWidth) property measure document width differently. The width of the **div** is set to 200, and this is the value retrieved by the **offsetWidth** property, not the **clientWidth** property.

    <DIV ID=oDiv STYLE="overflow:scroll; width:200; height:100"> . . . </DIV>
    <BUTTON onclick="alert(oDiv.clientWidth)">client width</BUTTON>
    <BUTTON onclick="alert(oDiv.offsetWidth)">offset widthY</BUTTON>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientWidth.htm)

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

