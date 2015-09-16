---
title: 'clientX'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - compatibility
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MouseEvent
    href: /dom/MouseEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the user agent''s client area).'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
uri: dom/MouseEvent/clientX

---
## Summary

Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the user agent's client area).

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var xCoordinate = event.clientX;
```

## Return Value

Returns an object of type NumberNumber

The X coordinate of the mouse cursor.

## Examples

This example uses the **clientX** property to determine the mouse position relative to the window. The console shows the mouse position at all times.

``` html
<!doctype html>
<html>
 <head>
  <script>
function logClientCoords() {
  console.log("The x coordinate is: " + e.clientX + "The y coordinate is: " + e.clientY);
}
function logCursorPosition(e) {
  console.log("X = " + e.clientX + " Y = ' + e.clientY);
}
window.addEventListener("move", logCursorPosition, false);
window.addEventListener("click", logClientCoords, false)
  </script>
 </head>
 <body>
 </body>
</html>
```

## Notes

Client coordinates do not reflect the scroll offset of the page. To get the mouse pointer's coordinates relative to the upper-left corner of the document, use the [**pageX**](/css/cssom/properties/pageX) and [**pageY**](/css/cssom/properties/pageY) properties.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
