---
title: 'scrollWidth'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollWidth.htm'
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
uri: dom/HTMLElement/scrollWidth

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.scrollWidth;
element.scrollWidth = value;
```

## Examples

When the [**overflow**](/css/properties/overflow) property is set to **auto**, the content can exceed the dimensions of an element, and scroll bars appear. You can use the **scrollWidth** property to retrieve the width of the content within the element.

This example uses the **scrollWidth** property to compare the viewable width of the content to the actual width of a **div** element. The width of the element is exposed through the [**offsetWidth**](/dom/HTMLElement/offsetWidth) property.

``` html
<script type="text/javascript">
function fnCheckScroll() {
   var iScrollWidth = oDiv.scrollWidth;
   var iOffsetWidth = oDiv.offsetWidth;
   var iDifference = iScrollWidth - iOffsetWidth;
   alert("Width: " + iOffsetWidth
      + "\nscrollWidth: " + iScrollWidth
      + "\nDifference: " + iDifference);
}
</script>
...
<div id="oDiv" style="overflow: scroll; height= 50px; width= 400px; text-align: left" nowrap>
    ...
</div>
<button onclick="fnCheckScroll()">Check scrollWidth</button>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollWidth.htm)

## Notes

### Remarks

The width is the distance between the left and right edges of the object's visible content. This property is read-only on HTML documents, and read-write on fixed regions. For more information about how to access the dimension and location of objects on the page through the Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

### Syntax
