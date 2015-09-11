---
title: CanvasRenderingContext2D
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/DOM/CanvasRenderingContext2D)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The 2D rendering context for the drawing surface of a &lt;canvas&gt; element.'
tags:
  0: API
  1: Objects
  3: Canvas
uri: apis/canvas/CanvasRenderingContext2D

---
## <span>Summary</span>

The 2D rendering context for the drawing surface of a &lt;canvas&gt; element.

## <span>Properties</span>

API Name
:   Summary

[html/elements/canvas](/apis/canvas/CanvasRenderingContext2D/canvas)
:   A (read-only) reference to the *canvas* element that the CanvasRenderingContext2D object was created for.

[fillStyle](/apis/canvas/CanvasRenderingContext2D/fillStyle)
:   The current style used to fill shapes. The style can be a [CanvasGradient](/apis/canvas/CanvasGradient), a [CanvasPattern](/apis/canvas/CanvasPattern), or a string containing a CSS color.

[font](/apis/canvas/CanvasRenderingContext2D/font)
:   The current canvas context font and characteristics, in the manner of the CSS *font* property.

[globalAlpha](/apis/canvas/CanvasRenderingContext2D/globalAlpha)
:   An alpha value that is applied to shapes and images before they are composited onto the canvas.

[globalCompositeOperation](/apis/canvas/CanvasRenderingContext2D/globalCompositeOperation)
:   Sets how shapes and images are drawn onto the existing bitmap once they have had globalAlpha and the current transformation matrix applied.

[lineCap](/apis/canvas/CanvasRenderingContext2D/lineCap)
:   Defines the type of endings the user agent will place on the end of lines.

[lineDashOffset](/apis/canvas/CanvasRenderingContext2D/lineDashOffset)
:   Specifies the number of pixels to offset the dash pattern.

[lineJoin](/apis/canvas/CanvasRenderingContext2D/lineJoin)
:   Defines the type of corners the user agent will place where two lines meet.

[lineWidth](/apis/canvas/CanvasRenderingContext2D/lineWidth)
:   The current line width, in coordinate space units.

[miterLimit](/apis/canvas/CanvasRenderingContext2D/miterLimit)
:   The current miter limit ratio.

[shadowBlur](/apis/canvas/CanvasRenderingContext2D/shadowBlur)
:   Specifies the level of the blurring effect. The units do not map to coordinate space units, and are not affected by the current transformation matrix.

[shadowColor](/apis/canvas/CanvasRenderingContext2D/shadowColor)
:   The color of the shadow.

[shadowOffsetX](/apis/canvas/CanvasRenderingContext2D/shadowOffsetX)
:   Specifies the distance that the shadow will be offset in the positive horizontal distance, in coordinate space units.

[shadowOffsetY](/apis/canvas/CanvasRenderingContext2D/shadowOffsetY)
:   Specifies the distance that the shadow will be offset in the positive vertical distance, in coordinate space units.

[strokeStyle](/apis/canvas/CanvasRenderingContext2D/strokeStyle)
:   The current style for stroking shapes. The style can be a [CanvasGradient](/apis/canvas/CanvasGradient), a [CanvasPattern](/apis/canvas/CanvasPattern), or a string containing a CSS color.

[textAlign](/apis/canvas/CanvasRenderingContext2D/textAlign)
:   Returns or sets the text alignment value. See return value description below.

[textBaseline](/apis/canvas/CanvasRenderingContext2D/textBaseline)
:   Returns or sets the baseline value. See return value description below.

## <span>Methods</span>

API Name
:   Summary

[addHitRegion](/apis/canvas/CanvasRenderingContext2D/addHitRegion)
:   Creates a hit region.

[arc](/apis/canvas/CanvasRenderingContext2D/arc)
:   Draws the specified arc.

[arcTo](/apis/canvas/CanvasRenderingContext2D/arcTo)
:   Check to be sure there's a subpath for (x1, y1). Then, the behavior depends on the arguments and the last point in the subpath. See Notes.

[beginPath](/apis/canvas/CanvasRenderingContext2D/beginPath)
:   Empties the list of subpaths in the context's current default path so that it once again has zero subpaths.

[bezierCurveTo](/apis/canvas/CanvasRenderingContext2D/bezierCurveTo)
:   Ensures there is a subpath for *(cp1x, cp1y)*, then connects the last point in the subpath to the given point *(x, y)* using a cubic Bézier curve with control points *(cp1x, cp1y)* and *(cp2x, cp2y)*, then adds the point *(x, y)* to the subpath.

[clearRect](/apis/canvas/CanvasRenderingContext2D/clearRect)
:   Clears all pixels on the canvas in the given rectangle *(x, y, w, h)* to transparent black.

[clip](/apis/canvas/CanvasRenderingContext2D/clip)
:   Specifies a new clipping region by calculating the intersection of the current clipping region and the area described by the intended path, using the non-zero winding number rule. The new clipping region replaces the current clipping region.

[closePath](/apis/canvas/CanvasRenderingContext2D/closePath)
:   Marks the last subpath as closed, creates a new subpath whose first point is the same as the previous subpath's last point, and then adds the new subpath to the path, returning to the first subpath's first point (closing the shape). If the object's path has no subpaths, this method does nothing.

[createImageData](/apis/canvas/CanvasRenderingContext2D/createImageData)
:   Depending on how it is called, returns either an **ImageData** object with the given *sw, sh* dimensions or an **ImageData** object with the same dimensions as the *imagedata* argument. See Notes.

[createLinearGradient](/apis/canvas/CanvasRenderingContext2D/createLinearGradient)
:   Returns a linear **CanvasGradient** initialized with the specified line as represented by the start point (*x0, y0*) and end point (*x1, y1*) of the gradient.

[createPattern](/apis/canvas/CanvasRenderingContext2D/createPattern)
:   Returns a **CanvasPattern** object that uses the given *image* and repeats in the direction(s) given by the *repetition* argument.

[createRadialGradient](/apis/canvas/CanvasRenderingContext2D/createRadialGradient)
:   Returns a radial **CanvasGradient** initialized with the two specified circles. This effectively creates a cone, touched by the two circles defined in the creation of the gradient, with the part of the cone before the start circle (0.0) using the color of the first offset, the part of the cone after the end circle (1.0) using the color of the last offset, and areas outside the cone (untouched by the gradient) transparent black.

[drawCustomFocusRing](/apis/canvas/CanvasRenderingContext2D/drawCustomFocusRing)
:   Draw a focus ring of the appropriate style along the intended path, and sets result to *false*.

    **Removed from spec; deletion candidate.**

[drawImage](/apis/canvas/CanvasRenderingContext2D/drawImage)
:   Draws the specified image onto the canvas. Can be called in three ways; see Notes.

[drawSystemFocusRing](/apis/canvas/CanvasRenderingContext2D/drawSystemFocusRing)
:   Draws a focus ring of the appropriate style along the intended path, following platform conventions.

    **Removed from spec; deletion candidate.**

[ellipse](/apis/canvas/CanvasRenderingContext2D/ellipse)
:   Draws the specified ellipse. If the object's path has any subpaths, this method adds a straight line from the last point in the subpath to the start point of the arc. Then, it adds the start and end points of the arc to the subpath, and connects them with an arc.

    **Experimental, subject to change or removal; deletion candidate.**

[fill](/apis/canvas/CanvasRenderingContext2D/fill)
:   Fills all the subpaths of the intended path, using *fillStyle*, and using the non-zero winding number rule. Open subpaths must be implicitly closed when being filled (without affecting the actual subpaths).

[fillRect](/apis/canvas/CanvasRenderingContext2D/fillRect)
:   Paints the specified rectangular area using the color (or style) defined by *[fillStyle](/apis/canvas/CanvasRenderingContext2D/fillStyle)*.

[fillText](/apis/canvas/CanvasRenderingContext2D/fillText)
:   Renders the given text at the given (x, y) coordinates, ensuring that the text isn't wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.

[getImageData](/apis/canvas/CanvasRenderingContext2D/getImageData)
:   Returns an ImageData object representing the underlying pixel data for the area of the canvas denoted by the rectangle whose corners are the four points (sx, sy), (sx+sw, sy), (sx+sw, sy+sh), (sx, sy+sh), in canvas coordinate space units.

[getLineDash](/apis/canvas/CanvasRenderingContext2D/getLineDash)
:   Gets the line dash properties for the stroke, as an array.

[isPointInPath](/apis/canvas/CanvasRenderingContext2D/isPointInPath)
:   Returns true if the point given by the x and y coordinates passed to the method, when treated as coordinates in the canvas coordinate space unaffected by the current transformation, is inside the intended path as determined by the non-zero winding number rule; returns false otherwise. If either of the arguments is infinite or NaN, then the method returns false.

[lineTo](/apis/canvas/CanvasRenderingContext2D/lineTo)
:   Connects the last point in the subpath to the given point (x, y) using a straight line, and then adds the point to the subpath.

[moveTo](/apis/canvas/CanvasRenderingContext2D/moveTo)
:   Creates a new subpath with the specified point as its first (and only) point.

[putImageData](/apis/canvas/CanvasRenderingContext2D/putImageData)
:   Writes data from ImageData structures back to the canvas. If any of the arguments are infinite or NaN, the method must throw a NotSupportedError exception. When the last four arguments are omitted, they are assumed to have the values 0, 0, the width member of the imagedata structure, and the height member of the imagedata structure, respectively.

[quadraticCurveTo](/apis/canvas/CanvasRenderingContext2D/quadraticCurveTo)
:   Ensures there is a subpath for (cpx, cpy), then connects the last point in the subpath to the given point (x, y) using a quadratic Bézier curve with control point (cpx, cpy), and then adds the given point (x, y) to the subpath.

[rect](/apis/canvas/CanvasRenderingContext2D/rect)
:   Creates a new subpath containing just the four points (x, y), (x+w, y), (x+w, y+h), (x, y+h), with those four points connected by straight lines, then marks the subpath as closed. It then creates a new subpath with the point (x, y) as the only point in the subpath.

[removeHitRegion](/apis/canvas/CanvasRenderingContext2D/removeHitRegion)
:   Removes a previously-defined hit region.

[restore](/apis/canvas/CanvasRenderingContext2D/restore)
:   Pops the top entry from the drawing state stack, and reset the drawing state it describes. If there is no saved state, the method does nothing.

[rotate](/apis/canvas/CanvasRenderingContext2D/rotate)
:   Addd the rotation transformation described by the argument to the transformation matrix. The *angle* argument represents a clockwise rotation angle expressed in radians.

[save](/apis/canvas/CanvasRenderingContext2D/save)
:   Saves the current state of the context. Use the restore() method to retrieve the saved state.

[scale](/apis/canvas/CanvasRenderingContext2D/scale)
:   Adds the scaling transformation described by the arguments to the transformation matrix. The *x* argument represents the scale factor in the horizontal direction; the *y* argument represents the scale factor in the vertical direction. The factors are multiples.

[scrollPathIntoView](/apis/canvas/CanvasRenderingContext2D/scrollPathIntoView)
:   Scrolls the current path into view. See Notes.

[setLineDash](/apis/canvas/CanvasRenderingContext2D/setLineDash)
:   Sets the line dash properties for the stroke.

[setTransform](/apis/canvas/CanvasRenderingContext2D/setTransform)
:   Resets the current transform to the identity matrix, and then invokes the *transform(a, b, c, d, e, f)* method with the same arguments.

[stroke](/apis/canvas/CanvasRenderingContext2D/stroke)
:   Traces the intended path, using the CanvasRenderingContext2D object for the line styles, and then fills the combined stroke area using the strokeStyle attribute.

[strokeRect](/apis/canvas/CanvasRenderingContext2D/strokeRect)
:   Takes the result of tracing the path, using the CanvasRenderingContext2D object's line styles, and fills it with the strokeStyle.

[strokeText](/apis/canvas/CanvasRenderingContext2D/strokeText)
:   Renders the given text at the given (x, y) coordinates, ensuring that the text isn't wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.

[transform](/apis/canvas/CanvasRenderingContext2D/transform)
:   Replaces the current transformation matrix with the result of multiplying the current transformation matrix with the matrix described by:

    `a c e b d f 0 0 1`

[translate](/apis/canvas/CanvasRenderingContext2D/translate)
:   Modifies the transformation matrix of this context by adding the scaling transformation described by the arguments to the transformation matrix. The arguments represent the scale factors in the horizontal (*x*) and vertical (*y*) directions. The factors are multiples.

## <span>Events</span>

*No events.*

## <span>Examples</span>

To get this object, call getContext() on a \<canvas\>, supplying "2d" as the argument:

``` js
var canvas = document.getElementById('MyCanvas');
var ctx = canvas.getContext('2d');
// draw a green rect
ctx.fillStyle = "lime";
ctx.fillRect(10, 10, 100, 100);
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
