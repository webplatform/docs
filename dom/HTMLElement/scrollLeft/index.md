---
title: 'scrollLeft'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
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
uri: dom/HTMLElement/scrollLeft

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.scrollLeft;
element.scrollLeft = value;
```

## Examples

This example uses the **scrollLeft** property to determine the amount scrolled by the object.

``` html
<DIV ID=oDiv STYLE="position:absolute; width:200px;
    height:100px; overflow:scroll"
    onclick=alert(this.scrollLeft)>
<SPAN STYLE="width:250px"> . . . </SPAN></DIV>
```

## Notes

### Remarks

This property's value equals the current horizontal offset of the content within the scrollable range. Although you can set this property to any value, if you assign a value less than 0, the property is set to 0. If you assign a value greater than the maximum value, the property is set to the maximum value. You can set this property inline, but the results might be inconsistent while the document loads. This property is always 0 for objects that do not have scroll bars. For these objects, setting the property has no effect. When a **marquee** object scrolls vertically, its **scrollLeft** property is set to 0, overriding any script setting. For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Object Model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

### Syntax
