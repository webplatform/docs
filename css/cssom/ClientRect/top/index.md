---
title: top
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
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
summary: 'Returns the top value for a ClienRect object.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/ClientRect/top

---
## Summary

Returns the top value for a ClienRect object.

Property of [css/cssom/ClientRect](/css/cssom/ClientRect)[css/cssom/ClientRect](/css/cssom/ClientRect)

## Syntax

**Note**: This property is read-only.

``` js
var pixelsFromTop = clientRect.top;
```

## Return Value

Returns an object of type NumberNumber

## Examples

This example uses the [**getBoundingClientRect**](/dom/HTMLElement/getBoundingClientRect) method to retrieve the coordinates of the bounds of the text rectangles within the element.

``` html
<SCRIPT>
function getCoords(oObject) {
    oBndRct=oObject.getBoundingClientRect();
    alert("Bounding rectangle = \nUpper left coordinates: "
        + oBndRct.left + " " + oBndRct.top +
        "\nLower right coordinates: "
        + oBndRct.right + " " + oBndRct.bottom);
}
</SCRIPT>
</HEAD>
<BODY>
<P ID=oPara onclick="getCoords(this)">
```

## Notes

Use this syntax to access the top coordinate of the second text rectangle of a [**TextRange**](/dom/TextRange) object:

    oRct = oTextRange.getClientRects();
    oRct[1].top;

Note that the collection index starts at 0, so the second item index is 1. To access the top coordinate of the bounding rectangle of an object, use this syntax:

    oBndRct = oElement.getBoundingClientRect();
    oBndRct.top;
