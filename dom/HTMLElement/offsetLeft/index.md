---
title: 'offsetLeft'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetLeft.htm'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/offsetLeft

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.offsetLeft;
element.offsetLeft = value;
```

## Examples

This example uses the **offsetLeft** property to determine whether an object is in the user's view.

``` html
<script type="text/javascript">
function isinView(element) {
    var oparent = element.offsetParent;
    var osleft = oID_1.offsetLeft;
    var cleft = oparent.clientWidth;
    if (osleft > cleft) {
        alert("Expand the window to see the paragraph!");
    }
}
</script>
...
<button onclick="isinView(this)">Click here</button>
...
<div id="oID_1" style="position: absolute; top:200px; left:1200px;">
...
</div>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetLeft.htm)

## Notes

### Remarks

You can determine the location, width, and height of an object by using a combination of the **offsetLeft**, [**offsetTop**](/dom/HTMLElement/offsetTop), [**offsetHeight**](/dom/HTMLElement/offsetHeight), and [**offsetWidth**](/dom/HTMLElement/offsetWidth) properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent. For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

### Syntax
