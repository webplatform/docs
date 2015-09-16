---
title: bottom
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectangles.htm'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/ClientRect
    href: /css/cssom/ClientRect
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /css/cssom/ClientRect
summary: 'Returns the bottom value for a ClienRect object.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/ClientRect/bottom

---
## Summary

Returns the bottom value for a ClienRect object.

Property of [css/cssom/ClientRect](/css/cssom/ClientRect)[css/cssom/ClientRect](/css/cssom/ClientRect)

## Syntax

**Note**: This property is read-only.

``` js
var pixelsFromBottom = clientRect.bottom;
```

## Return Value

Returns an object of type NumberNumber

The number of pixels.

## Examples

This example uses the [**getBoundingClientRect**](/dom/HTMLElement/getBoundingClientRect) method to retrieve the coordinates of the bounds of the text rectangles within the element.

``` html
<!doctype html>
<html>
 <head>
  <title><title>
  <script>
function getCoords() {
  oBndRct=this.getBoundingClientRect();
  console.log("Bounding rectangle = \nUpper left coordinates: " +
    oBndRct.left + " " + oBndRct.top +
    "\nLower right coordinates: " +
    oBndRct.right + " " + oBndRct.bottom);
}
window.addEventListener("load", getCoords, false);
  </script>
 </head>
 <body>
  <p ></p>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectangles.htm)

## Notes

This syntax shows how to access the bottom coordinate of the second text rectangle of a [**TextRange**](/dom/TextRange) oTextRange object.

    oRct = oTextRange.getClientRects();
    oRct[1].bottom;

Note that the collection index starts at 0, so the second item index is 1. This syntax shows how to access the bottom coordinate of the bounding rectangle of an oElement element object.

    oBndRct = oElement.getBoundingClientRect();
    oBndRct.bottom;
