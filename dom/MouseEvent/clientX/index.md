---
title: clientX
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - compatibility
summary: 'Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the user agent''s client area).'
uri: dom/MouseEvent/clientX

---
# clientX

## Summary

Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the user agent's client area).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MouseEvent](/dom/MouseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var xCoordinate = event.clientX;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The X coordinate of the mouse cursor.

## Examples

This example uses the **clientX** property to determine the mouse position relative to the window. The console shows the mouse position at all times.

``` {.html}
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

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

