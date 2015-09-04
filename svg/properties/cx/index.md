---
title: cx
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'Unreviewed MSDN import'
uri: svg/properties/cx

---
# cx

## Examples

The following code example demonstrates how the starting point and direction of an arc for an ellipse are affected by a user space transform.



    <?xml version="1.0" standalone="no"?>
    <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
      "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
    <svg width="400px" height="300px" viewBox="0 0 400 300" xmlns="http://www.w3.org/2000/svg" version="1.1"
         xmlns:xlink="http://www.w3.org/1999/xlink">
      <desc>Arc Transform</desc>
      <!-- Show the outline of the canvas by using a rect element. -->
      <rect x="1" y="1" width="399" height="299" fill="none" stroke="black" stroke-width="1" />
      <defs>
        <ellipse id="theEllipse" x="0" y="0" rx="50" ry="100" style="fill: blue; stroke: black; stroke-width: 5px;"/>
      </defs>
      <use xlink:href="#theEllipse" x="90" y="150"/>
      <!-- transform="rotate(30, 280, 150)" rotates the ellipse 30 degrees about the
           point (280, 150) as opposed to the origin of the viewport. -->
      <use xlink:href="#theEllipse" x="280" y="150" transform="rotate(30, 280, 150)"/>
     </svg>

</pre>

## Notes

### Remarks

The arc of a [**circle**](/svg/elements/circle) element and the arc of an [**ellipse**](/svg/elements/ellipse) element begin at the 3 o'clock point on the associated radius and progress towards the 9 o'clock point. The starting point and direction of the arc are affected by the user space transform in the same manner as the geometry of the element.

### Syntax

### Standards information

-   [Scalable Vector Graphics (SVG) 1.1](http://go.microsoft.com/fwlink/p/?linkid=190918), Appendix M

## See also

### Related pages (MSDN)

-   [**SVGCircleElement**](/svg/elements/circle)
-   [**SVGEllipseElement**](/svg/elements/ellipse)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

