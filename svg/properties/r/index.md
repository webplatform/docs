---
title: r
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/r

---
## Examples

The following code example creates a 200 × 200 pixel viewport and draws a red, 50 px-radius circle that has a black border. If you move the mouse pointer over the rendered circle, the circle doubles its radius; if you move the mouse pointer off the rendered circle, the circle's current radius reduces by half. The rectangle element is used to outline the boundaries of the viewport.

``` html


<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
  <title>Manipulating the Radius of an SVG Circle</title>
  <script language="javascript" type="text/javascript">
    var red_circle;  // An object that represents the circle.
    var r;           // A variable that represents the circle's radius.

    window.onload = function() {
      red_circle = document.getElementById('redCircle');
      r = parseInt(red_circle.getAttribute("r"));
    }

    function grow() {
      r = 2*r;
      red_circle.setAttribute("r",r);
    }

    function shrink() {
      r = r/2;
      red_circle.setAttribute("r",r);
    }
  </script>
</head>
<body>
  <svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="200px" height="200px">
    <circle id="redCircle" cx="100" cy="100" r="50" style="stroke: black; fill: red;" onmouseover="grow()" onmouseout="shrink()"/>
    <rect x="0" y="0" width="100%" height="100%" style="fill: none; stroke: black;"/>
  </svg>
</body>
</html>
```

</pre>
[To make this example work across browsers, save this code example with a .xhtml extension. View live example]

### Syntax

### Standards information

-   [Scalable Vector Graphics: Basic Shapes](http://go.microsoft.com/fwlink/p/?linkid=204737), Section 9.8.2

## See also

### Related pages (MSDN)

-   [**SVGCircleElement**](/svg/elements/circle)
