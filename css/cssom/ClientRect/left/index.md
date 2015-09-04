---
title: left
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Returns the left value for a ClienRect object.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectangles.htm'
uri: css/cssom/ClientRect/left

---
# left

## Summary

Returns the left value for a ClienRect object.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/ClientRect](/css/cssom/ClientRect)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var pixelsFromLeft = clientRect.left;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The number of pixels.

## Examples

This example uses the [**getBoundingClientRect**](/dom/HTMLElement/getBoundingClientRect) method to retrieve the coordinates of the bounds of the text rectangles within the element.

``` {.html}
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

