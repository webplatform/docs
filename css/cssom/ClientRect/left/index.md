---
title: left
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
summary: 'Returns the left value for a ClienRect object.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/ClientRect/left

---
## Summary

Returns the left value for a ClienRect object.

Property of [css/cssom/ClientRect](/css/cssom/ClientRect)[css/cssom/ClientRect](/css/cssom/ClientRect)

## Syntax

**Note**: This property is read-only.

``` js
var pixelsFromLeft = clientRect.left;
```

## Return Value

Returns an object of type NumberNumber

The number of pixels.

## Examples

This example uses the [**getBoundingClientRect**](/dom/HTMLElement/getBoundingClientRect) method to retrieve the coordinates of the bounds of the text rectangles within the element.

``` html
<SCRIPT>
function getCoords(oObject) {
    oBndRct=oObject.getBoundingClientRect();
    alert("Bounding rectangle = \nUpperleft coordinates: "
        + oBndRct.left + " " + oBndRct.top +
        "\nLowerright coordinates: "
        + oBndRct.right + " " + oBndRct.bottom);
}
</SCRIPT>
</HEAD>
<BODY>
<P ID=oPara onclick="getCoords(this)">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectangles.htm)

## Notes

To access the left coordinate of the second text rectangle of a [**TextRange**](/dom/TextRange) object, use this syntax:

    oRct = oTextRange.getClientRects();
    oRct[1].left;

Note that because the collection index starts at 0, the second item index is 1. To access the left coordinate of the bounding rectangle of an element object, use this syntax:

    oBndRct = oElement.getBoundingClientRect();
    oBndRct.left;
