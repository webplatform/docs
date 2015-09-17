---
title: 'clientHeight'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientHeight.htm'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/clientHeight

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.clientHeight;
element.clientHeight = value;
```

## Examples

This example shows how the **clientHeight** property and the [**offsetHeight**](/dom/HTMLElement/offsetHeight) property measure document height differently. The height of the **div** is set to 100, and this is the value retrieved by the **offsetHeight** property, not the **clientHeight** property.

``` html
<div id="oDiv" style="overflow: scroll; width: 200px; height: 100px">
    . . . </div>
<button onclick="alert(oDiv.clientHeight)">client height</button>
<button onclick="alert(oDiv.offsetHeight)">offset heightY</button>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clientHeight.htm)

### Syntax
