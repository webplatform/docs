---
title: perspective
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines how many pixels away a 3D element is placed from the viewer. This allows you to change the apparent perspective of how 3D elements are viewed.'
tags:
  - CSS
  - Functions
uri: css/functions/perspective

---
## <span>Summary</span>

Defines how many pixels away a 3D element is placed from the viewer. This allows you to change the apparent perspective of how 3D elements are viewed.

## <span>Examples</span>

The following code snippet is an example of the **perspective** function in use. When applied to a square blue [**div**](/html/elements/div) element along with the [**translateZ**](/css/functions/translateZ()) function (which enables the specified element to appear to have moved away from the viewer), it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)

``` html
div {
  transform: perspective(500px) translateZ(-60px);
}
```

## <span>Notes</span>

### <span>Remarks</span>

The value must be greater than 0 and is given in pixels.

For more information about transformation matrices, see [Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246), in the [CSS3 Transforms](http://go.microsoft.com/fwlink/?LinkID=223145) specification. The **perspective** function is often necessary for other 3-D transformation functions to have a visible effect.

### <span>Syntax</span>

**perspective** `( <length> )`

### <span>Parameters</span>

*length*
:   Value in pixels that specifies a perspective projection matrix. This value is expressed as a number followed by "px".

### <span>Standards information</span>

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 3-D Transforms`
