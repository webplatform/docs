---
title: clientWidth
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientWidth.htm'
notes:
  - 'summary, examples best practices, compatibility, standards, clean-up of MSDN sections'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/clientWidth

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.clientWidth;
element.clientWidth = value;
```

## <span>Examples</span>

This example shows how the **clientWidth** property and the [**offsetWidth**](/dom/HTMLElement/offsetWidth) property measure document width differently. The width of the **div** is set to 200, and this is the value retrieved by the **offsetWidth** property, not the **clientWidth** property.

``` html
<DIV ID=oDiv STYLE="overflow:scroll; width:200; height:100"> . . . </DIV>
<BUTTON onclick="alert(oDiv.clientWidth)">client width</BUTTON>
<BUTTON onclick="alert(oDiv.offsetWidth)">offset widthY</BUTTON>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientWidth.htm)

### <span>Syntax</span>