---
title: 'SVG grand tour'
notes:
  - 'Fix multiple broken links'
readiness: 'In Progress'
summary: 'This guide shows you how to build a pair of animating eyeballs, providing a comprehensive tour of SVG features detailed in other tutorials. It shows how to maintain a set of reusable graphic components, and provides essential context on SVG transforms and coordinate spaces.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/attributes/cx
    - svg/attributes/cy
    - svg/attributes/r
    - svg/properties/fill
    - svg/properties/stroke
    - svg/attributes/id
    - svg/properties/font-size
    - svg/attributes/style
    - svg/attributes/class
    - svg/attributes/d
    - svg/properties/clip-path
    - svg/properties/stroke-width
    - svg/properties/stroke-dasharray
    - svg/properties/stroke-linejoin
    - svg/attributes/x
    - svg/attributes/y
    - svg/attributes/width
    - svg/attributes/height
    - svg/attributes/filterUnits
    - svg/attributes/transform
    - svg/attributes/viewBox
    - svg/attributes/preserveAspectRatio
    - svg/elements/animate
    - svg/attributes/attributeType
    - svg/attributes/attributeName
    - svg/attributes/begin
    - svg/attributes/dur
    - svg/attributes/from
    - svg/attributes/to
    - svg/attributes/end
    - svg/attributes/startOffset
    - svg/properties/fill-opacity
    - svg/properties/stroke-opacity
uri: 'svg/tutorials/smarter svg overview'

---
**By Mike Sierra**

## Summary

This guide shows you how to build a pair of animating eyeballs, providing a comprehensive tour of SVG features detailed in other tutorials. It shows how to maintain a set of reusable graphic components, and provides essential context on SVG transforms and coordinate spaces.

SVG is a standard markup format, like HTML and XML, that renders *Scalable Vector Graphics* within web browsers. *Vector* or *drawing*-style graphics are implemented as pure shapes that render crisply at any magnification. In contrast, *raster* or *paint*-style images consist of a series of pixels that may not display well when zoomed at high resolution. Use SVG if you want to freely interact with portions of a graphic. Since SVG renders within the browser's DOM, each graphic component can be styled through CSS, manipulated with JavaScript through core APIs, and can appear comfortably within HTML pages.

This section of the guide shows how SVG is deployed along with other core web standards, with which you should already be familiar. It highlights some notable differences, and provides a quick tour of many SVG features that are covered in more detail in other sections. It focuses on the unique way you can build complex interactive graphics from reusable components, and how to flexibly resize them and place them within various drawing surfaces.

![scr svg eyes.png](//static.webplatform.org/a/a7/scr_svg_eyes.png)

As part of a grand tour to get a feel for SVG markup, you'll stroll through an example that shows how to build a pair of eyes, and how to move them around and make them blink. [View the accompanying live demo here](http://letmespellitoutforyou.com/samples/svg_eyeball.html).

## Defining the drawing area

There are several ways to deploy SVG, with various options outlined in the section at the bottom of this page. Examples used throughout this guide feature *inline* SVG that's directly embedded within HTML, which allows you to flexibly apply CSS and JavaScript to both the SVG graphic and the HTML content. The basic markup looks like this, with an [**svg**](/svg/elements/svg) element encapsulating the graphics:

``` html
<!DOCTYPE html>
<html>
<head>
<title>SVG grand tour demo</title>
<link href="css/eyeballs.css" rel="stylesheet" />
</head>
<body>
<svg width="600" height="200">
   <title>eyeballs</title>
   <desc>interactive demo showcasing several SVG features</desc>
</svg>
<script src="js/eyeballs.js"></script>
</body>
</html>
```

 You can add [**title**](/svg/elements/title) and [**desc**](/svg/elements/desc) elements wherever necessary to comment your markup.

(See [**SVG deployment**](/svg/tutorials/smarter_svg_deploy) for different ways to render SVG content.)

## The eyeball

Adding this line within the [**svg**](/svg/elements/svg) region produces a circle. The [**cx**](/w/index.php?title=svg/attributes/cx&action=edit&redlink=1) and [**cy**](/w/index.php?title=svg/attributes/cy&action=edit&redlink=1) attributes position its center point, and the [**r**](/w/index.php?title=svg/attributes/r&action=edit&redlink=1) sizes it relative to that point:

``` xml
<circle id="eyeball" cx="100" cy="100" r="50"/>
```

 ![svgGrandTour eyeball circle black.png](//static.webplatform.org/thumb/3/31/svgGrandTour_eyeball_circle_black.png/100px-svgGrandTour_eyeball_circle_black.png)

By default, it's filled black. Adding a [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) attribute allows you to color the background white, and a [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) attribute helps clarify the edge of the shape:

``` xml
<circle id="eyeball" cx="100" cy="100" r="50" fill="white" stroke="black"/>
```

 ![svgGrandTour eyeball circle white.png](//static.webplatform.org/thumb/e/ec/svgGrandTour_eyeball_circle_white.png/100px-svgGrandTour_eyeball_circle_white.png)

To add the iris and pupil, you can add more circles that specify different fill colors. Declaring the larger circles first prevents them from obscuring the smaller ones:

``` xml
<circle id="eyeball" cx="100" cy="100" r="50" fill="white" stroke="black"/>
<circle id="iris"    cx="100" cy="100" r="25" fill="lightblue"/>
<circle id="pupil"   cx="100" cy="100" r="12" fill="black"/>
```

 ![svgGrandTour eyeball circles.png](//static.webplatform.org/thumb/9/96/svgGrandTour_eyeball_circles.png/100px-svgGrandTour_eyeball_circles.png)

(See [**SVG shapes**](/svg/tutorials/smarter_svg_shapes) for more about basic graphic elements such as circles, ellipses, rectangles, and polygons.)

## Styling via CSS

In this example, the [**id**](/w/index.php?title=svg/attributes/id&action=edit&redlink=1), [**cx**](/w/index.php?title=svg/attributes/cx&action=edit&redlink=1), [**cy**](/w/index.php?title=svg/attributes/cy&action=edit&redlink=1), and [**r**](/w/index.php?title=svg/attributes/r&action=edit&redlink=1) are all ordinary *attributes*, while the [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) and [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) are known as *presentation attributes*. These are simply CSS properties that happen to be expressed as attributes. Other than the tendency of longer CSS property names to use *dashes-between-lowercase-words* rather than *camelCase* for attribute names, there may be no way to tell the difference by looking at them.

Many CSS properties such as [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) and [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) apply only to SVG content. Some, like [**font-size**](/w/index.php?title=svg/properties/font-size&action=edit&redlink=1), apply to both SVG and HTML. Some behave like CSS properties that you apply to HTML, but are named differently. The [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) property provides much the same capabilities in SVG as the [**background-color**](/css/properties/background-color) and [**background-image**](/css/properties/background-image) properties do for HTML. Since [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) is a CSS property, You can also modify it locally via the [**style**](/w/index.php?title=svg/attributes/style&action=edit&redlink=1) attribute. Doing so actually takes precedence over the value of presentation attributes, so this example changes the eye color to brown:

``` xml
<circle id="iris" cx="100" cy="100" r="25" fill="lightblue" style="fill:brown"/>
```

 As in HTML, you can consolidate CSS within style sheets to separate it from markup. Placing this CSS in the *eyeballs.css* file referenced from the HTML applies it to the slightly pared-down SVG markup that follows:

``` css
#eyeball { fill: white; stroke: black }
#iris { fill: lightblue }
#pupil { fill: black }
```

``` xml
<circle id="eyeball" cx="100" cy="100" r="50"/>
<circle id="iris"    cx="100" cy="100" r="25"/>
<circle id="pupil"   cx="100" cy="100" r="12"/>
```

 As you'll see below, there are some cases where you want to avoid using style sheets.

(See [**SVG deployment**](/svg/tutorials/smarter_svg_deploy) for different ways to apply CSS.)

## Applying a gradient

The concentric circles provide a good way to implement the edge of the iris and pupil, but are not good for the slight bloodshot color towards the edge of the eye. As an alternative, you can implement the entire eyeball as a large circle, within which a radial gradient builds a series of concentric rings:

``` xml
<circle id="eyeball" cx="100" cy="100" r="150" fill="url(#eyeballFill)" />

<radialGradient id="eyeballFill">
  <stop id="inner"           offset="12%"  stop-color="black" />
  <stop id="pupil"           offset="15%"  stop-color="lightblue" />
  <stop id="iris"            offset="27%"  stop-color="lightblue" />
  <stop id="white"           offset="30%"  stop-color="white" />
  <stop id="bloodshotExtent" offset="40%"  stop-color="white" />
  <stop id="outer"           offset="100%" stop-color="pink" />
</radialGradient>
```

 ![svgGrandTour eyeball fill.png](//static.webplatform.org/thumb/1/1d/svgGrandTour_eyeball_fill.png/200px-svgGrandTour_eyeball_fill.png)

The [**circle**](/svg/elements/circle) element's [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) attribute uses CSS's **url()** function to reference the [**id**](/w/index.php?title=svg/attributes/id&action=edit&redlink=1) of the [**radialGradient**](/svg/elements/radialGradient) element. Its nested [**stop**](/svg/elements/stop) elements define fairly abrupt gradations from the center towards the edge—from black to blue and then to white—followed by a more gradual transition to pink around the edge of the circle. SVG gradients work similarly to CSS gradients available for HTML content, but CSS gradients are only available via the [**background-image**](/css/properties/background-image) property, which doesn't apply to SVG.

(See [**SVG graphics**](/svg/tutorials/smarter_svg_graphics) for details about gradients, and other information on using patterns and images.)

## Referencing graphics

This new circle is much larger than the actual eyeball, because we want to move it around behind a smaller pair of eyelids. (Don't worry for now that the shape is wider than the drawing area.) Before you build the eyelids, you should stash away the graphic components you've already defined. Add a [**defs**](/svg/elements/defs) region to the [**svg**](/svg/elements/svg):

``` html
<!DOCTYPE html>
<html>
<head>
<title>SVG grand tour demo</title>
<link href="css/eyeballs.css" rel="stylesheet" />
</head>
<body>
<svg width="600" height="200">
   <title>eyeballs</title>
   <desc>interactive demo showcasing several SVG features</desc>
   <defs>
      <!-- place components here -->
   </defs>
</svg>
<script src="js/eyeballs.js"></script>
</body>
</html>
```

 If you move the [**radialGradient**](/svg/elements/radialGradient) within the [**defs**](/svg/elements/defs) region, the [**circle**](/svg/elements/circle) still references it as before, but if you move the [**circle**](/svg/elements/circle) there, it doesn't render.

The SVG [**use**](/svg/elements/use) element allows you a way to reuse graphic components repeatedly, and to place them in differently sized areas. After placing the [**circle**](/svg/elements/circle) within the [**defs**](/svg/elements/defs) region, pointing to it with a [**use**](/svg/elements/use) element placed outside the [**defs**](/svg/elements/defs) makes it render:

``` xml
<use xlink:href="#eyeball"/>
```

 The [**use**](/svg/elements/use) element can be a bit mystifying at first. It's not simply a copy of the object it points to, but a *deep reference*. Any changes made to the prototype [**circle**](/svg/elements/circle) or [**radialGradient**](/svg/elements/radialGradient) components appears dynamically wherever a [**use**](/svg/elements/use) element references them. Despite this flexibility, you can't redefine any of the referenced object's attributes. But you can add optional presentation attributes that aren't already defined there.

Since the [**use**](/svg/elements/use) and its target element are placed in different parts of the document tree, CSS style sheets that ordinarily apply to the target do not automatically cascade to the [**use**](/svg/elements/use). However, you can apply CSS separately to the [**use**](/svg/elements/use) element. This example applies the same style sheet based on the [**id**](/w/index.php?title=svg/attributes/id&action=edit&redlink=1) of the target, and the [**class**](/w/index.php?title=svg/attributes/class&action=edit&redlink=1) of any [**use**](/svg/elements/use) that references it:

``` xml
<style>
#eyeball, .eyeball {
    fill: url(#eyeballFill);
}
</style>
<svg width="200" height="200">
<defs>
<circle id="eyeball" cx="100" cy="100" r="150" />
<defs>
<use xlink:href="#eyeball" class="eyeball" id="eyeball_1"/>
</svg>
```

 Note that if the targeted [**circle**](/svg/elements/circle) were also to share the same *eyeball* class in this example, then the [**use**](/svg/elements/use) element would not have the flexibility to be able to change it.

Notice as well that the [**use**](/svg/elements/use) element needs the **xlink** namespace to qualify the standard **href** attribute, which is also available in HTML with no namespace qualifier. This **xlink:href** attribute offers a different way to reference an object than the CSS **url()** syntax you see in the example above.

## The eyelids

To place the eyeball within eyelids requires a *clipping path*, which allows an object to render only when it appears within another shape. In this case, the *eyelids* shape is a free-form [**path**](/svg/elements/path) whose [**d**](/w/index.php?title=svg/attributes/d&action=edit&redlink=1) (*definition*) attribute draws two curves that face each other:

``` xml
<path id="eyelids" d="M 200,100 Q 100,200 0,100 Q 100,0 200,100" />
```

 ![svgGrandTour eyeball eyelid.png](//static.webplatform.org/thumb/f/fa/svgGrandTour_eyeball_eyelid.png/200px-svgGrandTour_eyeball_eyelid.png)

Each curve's definition includes *control points* that influence the shape of the curve, but that do not themselves render. Starting from the right corner (*M* for *move to*), the first quadratic (*Q*) curve's control point is placed at the top, and the destination is the left corner. The second quadratic curve places its control point at the bottom corner and ends up at the right corner:

![svgGrandTour eyeball ctrl.png](//static.webplatform.org/thumb/f/f6/svgGrandTour_eyeball_ctrl.png/200px-svgGrandTour_eyeball_ctrl.png)

To make the shape behave as a clipping path, place a [**clipPath**](/svg/elements/clipPath) element around the [**path**](/svg/elements/path). You will actually need to use this shape again, so it is best to [**use**](/svg/elements/use) a reference to it:

``` xml
<clipPath id="clipEyelid">
    <use xlink:href="#eyelids" class="eyelids" />
</clipPath>
```

 Now apply the [**clip-path**](/w/index.php?title=svg/properties/clip-path&action=edit&redlink=1) property to apply the clipping path to the eyeball shape. This example shows it assigned separately via CSS:

``` css
.eyeball {
    fill       : url(#eyeballFill);
    clip-path  : url(#clipEyelid);
}
```

``` xml
<use xlink:href="#eyeball" class="eyeball" />
```

 ![svgGrandTour eyeball eyelid clip.png](//static.webplatform.org/thumb/e/e1/svgGrandTour_eyeball_eyelid_clip.png/200px-svgGrandTour_eyeball_eyelid_clip.png)

The only problem now is that the eyelid has disappeared. Clipping paths don't actually render, so we need to point another reference to it. The first [**use**](/svg/elements/use) below places the eyeball within the clipping path, and the second produces the path itself. The third [**use**](/svg/elements/use) that appears outside the [**defs**](/svg/elements/defs) renders the entire object:

``` xml
<defs>
<g id="eye">
  <use xlink:href="#eyeball" class="eyeball" />
  <use xlink:href="#eyelids" class="eyelids" />
</g>
</defs>
<use xlink:href="#eye" />
```

 ![svgGrandTour eyeball eyelid both.png](//static.webplatform.org/thumb/f/f9/svgGrandTour_eyeball_eyelid_both.png/200px-svgGrandTour_eyeball_eyelid_both.png)

It becomes useful here to *group* the two graphic elements, wrapping a [**g**](/svg/elements/g) element around them to consolidate a larger semantic *eye* object. You can reference the grouped object, and you will see below, move or otherwise transform it as a unit.

(See [**SVG shapes**](/svg/tutorials/smarter_svg_shapes) for details on path commands, and [**SVG graphics**](/svg/tutorials/smarter_svg_graphics) for clipping paths.)

## The eyelashes

Drawing the eyelashes along the eyelid requires a bit of creativity. We need to add a third reference to the eyelid shape.

``` xml
<g id="eye">
  <use xlink:href="#eyelids" class="eyelashes" />
  <use xlink:href="#eyelids" class="eyelids"   />
  <use xlink:href="#eyeball" class="eyeball"   />
</g>
```

 The *eyelashes* class presents the underlying *eyelids* shape much differently:

``` css
.eyelashes {
    fill              : none;
    stroke            : #ddd;
    stroke-width      : 40;
    stroke-dasharray  : 1,10;
    stroke-linejoin   : bevel;
}
```

 The [**stroke-width**](/w/index.php?title=svg/properties/stroke-width&action=edit&redlink=1) thickens the edge so that it extends both inside and outside the shape. By default, the *stroke* is solid, but you can apply a *dash* pattern to break it into segments. Setting the [**stroke-dasharray**](/w/index.php?title=svg/properties/stroke-dasharray&action=edit&redlink=1) property to *1,10* specifies that for every pixel rendered around the edge of the shape, skip another ten pixels. This has the effect of drawing individual eyelashes:

![svgGrandTour eyeball eyelashes.png](//static.webplatform.org/thumb/d/d3/svgGrandTour_eyeball_eyelashes.png/200px-svgGrandTour_eyeball_eyelashes.png)

The beveled [**stroke-linejoin**](/w/index.php?title=svg/properties/stroke-linejoin&action=edit&redlink=1) property prevents the stroke from rendering too far past the sharp corner of the eye where the eyelids meet.

(See [**SVG shapes**](/svg/tutorials/smarter_svg_shapes) for details on various stroke properties.)

## Applying eyeliner

Even after lightening the color of the stroke, the eyelashes appear way too crisp and thin compared to the eyeball, and could be softened and thickened up a bit. SVG *filters* provide many image processing tools that you can mix and match to produce such special visual effects.

Add a [**filter**](/svg/elements/filter) element to the [**defs**](/svg/elements/defs) region. It serves as a wrapper for various *filter effect* components, which by default are applied in sequence. In this case, the [**feGaussianBlur**](/svg/elements/feGaussianBlur) effect scatters the pixels around randomly (a bit more vertically than horizontally), and [**feComponentTransfer**](/svg/elements/feComponentTransfer) darkens the result:

``` xml
<filter
    id           = "soften"
    x            = "-20"
    y            = "-20"
    width        = "250"
    height       = "250"
    filterUnits  = "userSpaceOnUse"
>
  <desc>soften eyelid and eyelashes</desc>
  <feGaussianBlur stdDeviation="1 3" />
  <feComponentTransfer>
      <feFuncR type="linear" slope="0.3"/>
      <feFuncG type="linear" slope="0.3"/>
      <feFuncB type="linear" slope="0.3"/>
  </feComponentTransfer>
</filter>
```

 Since the eyelid renders horizontally between 0 and 200 pixels, the eyelashes spill slightly outside the the left edge of the original drawing area. The *filter* element's [**x**](/w/index.php?title=svg/attributes/x&action=edit&redlink=1)/[**y**](/w/index.php?title=svg/attributes/y&action=edit&redlink=1)/[**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1)/[**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) attributes apply the effect to a wider set of dimensions. Setting [**filterUnits**](/w/index.php?title=svg/attributes/filterUnits&action=edit&redlink=1) to **userSpaceOnUse** uses the same coordinate system as the shape to which the filter is applied; otherwise values would be interpreted as percentages of the object's bounding box.

Use the [**filter**](/svg/properties/filter) property to assign the effect to the shape used to render the eyelids and eyelashes:

``` css
#eyelids {
    filter : url(#soften);
}
```

 Here is how it appears, first after the blur, then after the subsequent darkening:

![svgGrandTour eyeball eyelash filter blur.png](//static.webplatform.org/thumb/7/7d/svgGrandTour_eyeball_eyelash_filter_blur.png/200px-svgGrandTour_eyeball_eyelash_filter_blur.png)

![svgGrandTour eyeball eyelid filters.png](//static.webplatform.org/thumb/4/4f/svgGrandTour_eyeball_eyelid_filters.png/200px-svgGrandTour_eyeball_eyelid_filters.png)

(See [**SVG filters**](/svg/tutorials/smarter_svg_filters) for information on various ways to combine SVG's filter effects.)

## Transforms and coordinate spaces

To finish off the graphic, group another instance of the *eye* object into a higher-level *eyes* object:

``` xml
<g id="eyes">
  <use xlink:href="#eye"/>
  <use xlink:href="#eye"/>
</g>
```

 This renders the same shape twice at the same location. To space them out, apply a [**transform**](/w/index.php?title=svg/attributes/transform&action=edit&redlink=1). This moves the character's right eye to the right a bit, and the left eye 300 units further:

``` xml
<g id="eyes">
  <use xlink:href="#eye" id="eyeRight" transform="translate(50,0)"/>
  <use xlink:href="#eye" id="eyeLeft"  transform="translate(350,0)"/>
</g>
```

 The [**transform**](/w/index.php?title=svg/attributes/transform&action=edit&redlink=1) attribute's **translate()** function provides a flexible way to reposition objects referenced via [**use**](/svg/elements/use), but transforms can be applied to most any graphic element. SVG transforms provide the same functionality as two-dimensional CSS transforms. The **scale()** function accepts a decimal value to size the object, where *1* is the current size, *0* vanishes to a point, and values greater than 1 increase the size. The **rotate()** function accepts a *deg* or *rad* angle measurement that spins the object. The **skewX()** and **skewY()** also accepts an angle with which to shear the object horizontally or vertically. And **translate()** shifts the object's position.

Once the eyes are semantically grouped, a single [**use**](/svg/elements/use) element outside the [**defs**](/svg/elements/defs) region renders them:

``` xml
<use xlink:href="#eyes"/>
```

 ![svgGrandTour eyeballs.png](//static.webplatform.org/thumb/a/ac/svgGrandTour_eyeballs.png/500px-svgGrandTour_eyeballs.png)

When presenting the eyes with other interface elements, you may want to resize them. The original [**svg**](/svg/elements/svg) element specified that they should appear within a 600×200-pixel rectangle:

``` xml
<svg width="600" height="200">
```

 ![svgGrandTour eyeballs viewport large.png](//static.webplatform.org/thumb/d/d6/svgGrandTour_eyeballs_viewport_large.png/600px-svgGrandTour_eyeballs_viewport_large.png)

But what if that's much too big for the context in which they are to appear? If you shrink it down, using either [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1)/[**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) attributes or CSS, its dimensions no longer match the various measurements specified within the graphic:

``` xml
<style>
svg {
    width  : 300px;
    height : 100px;
}
</style>
    <!-- ...or... -->
<svg width="300" height="100">
```

 ![svgGrandTour eyeballs viewport small.png](//static.webplatform.org/thumb/b/bd/svgGrandTour_eyeballs_viewport_small.png/300px-svgGrandTour_eyeballs_viewport_small.png)

The solution is to define a custom box using the [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1) attribute. Doing so declares a set of abstract units for exclusive use *within* the graphic, which may bear no relation to the outer coordinate space in which the graphic is presented, to which the SVG's [**width**](/w/index.php?title=svg/attributes/width&action=edit&redlink=1) and [**height**](/w/index.php?title=svg/attributes/height&action=edit&redlink=1) apply:

``` xml
<svg width="300" height="100" viewBox="0 0 600 200">
```

 ![svgGrandTour eyeballs viewbox.png](//static.webplatform.org/thumb/8/84/svgGrandTour_eyeballs_viewbox.png/300px-svgGrandTour_eyeballs_viewbox.png)

Adding a [**preserveAspectRatio**](/w/index.php?title=svg/attributes/preserveAspectRatio&action=edit&redlink=1) attribute controls what happens in cases when the shape of the [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1) doesn't match the *viewport* within which the graphic appears. In this case, **xMidYMid** centers it and shrinks it enough for the entire graphic to appear:

``` xml
<svg width="100" height="100" viewBox="0 0 600 200" preserveAspectRatio="xMidYMid">
```

 ![svgGrandTour eyeballs viewbox preserve.png](//static.webplatform.org/thumb/0/04/svgGrandTour_eyeballs_viewbox_preserve.png/100px-svgGrandTour_eyeballs_viewbox_preserve.png)

## Glancing

The only remaining problem is that the graphic doesn't actually *do* anything. We want to make the eyes to *move*.

In many cases, you can use CSS techniques to animate numeric and color properties that apply to SVG. For example, here's a way to gradually change the eye color, by toggling between the gradient color stops' *blue* and *brown* classes:

``` css
 .blue  { stop-color   : lightblue; }
 .brown { stop-color   : brown; }
 stop {
    transition         : all 5s;
    -webkit-transition : all 5s;
    -moz-transition    : all 5s;
 }
```

 ![svgGrandTour eyeballs brown.png](//static.webplatform.org/thumb/e/e0/svgGrandTour_eyeballs_brown.png/500px-svgGrandTour_eyeballs_brown.png)

You can't use that familiar approach for SVG attributes. SVG has its own mechanism (based on the *SMIL* standard) to animate attribute values. We'll use it to make the eye glance to the side.

First, let's try to move the eye statically using a **translate()** transform described above:

``` xml
<circle id="eyeball" cx="100" cy="100" r="50" transform="translate(50,0)"/>
```

 ![svgGrandTour eyeballs translate50.png](//static.webplatform.org/thumb/f/f2/svgGrandTour_eyeballs_translate50.png/500px-svgGrandTour_eyeballs_translate50.png)

That certainly didn't do what we want. It moved the entire eyeball, including the clipping path behind which it is supposed to render. Instead, modify the [**cx**](/w/index.php?title=svg/attributes/cx&action=edit&redlink=1) attribute, which sets the position of the center of the circle:

``` xml
<circle id="eyeball" cx="150" cy="100" r="50"/>
```

 ![svgGrandTour eyeball glance.png](//static.webplatform.org/thumb/e/ea/svgGrandTour_eyeball_glance.png/500px-svgGrandTour_eyeball_glance.png)

That's much better. Now return the [**cx**](/w/index.php?title=svg/attributes/cx&action=edit&redlink=1) to its original value. To get it to move dynamically, place an [**animate**](/w/index.php?title=svg/elements/animate&action=edit&redlink=1) element within the *eyeball* object whose attribute you want to modify:

``` xml
<circle id="eyeball" cx="100" cy="100" r="150" >
    <animate
        id             = "glanceStart"
        attributeType  = "XML"
        attributeName  = "cx"
        begin          = "1s"
        dur            = "0.5s"
        from           = "100"
        to             = "150"
    />
</circle>
```

 Let's step through what each attribute does:

-   [**attributeType**](/w/index.php?title=svg/attributes/attributeType&action=edit&redlink=1) clarifies that the value we're manipulating is an *XML* attribute, not a *CSS* property.

-   [**attributeName**](/w/index.php?title=svg/attributes/attributeName&action=edit&redlink=1) provides the name of the attribute to modify, *cx* in this case.

-   [**begin**](/w/index.php?title=svg/attributes/begin&action=edit&redlink=1) specifies a delay after which the animation executes, in this case 1 second. A begin value of *0s* animates immediately. (If you leave out this attribute, the animation does not play by default, but you can control it with JavaScript as described below.)

-   [**dur**](/w/index.php?title=svg/attributes/dur&action=edit&redlink=1) specifies the animation's duration, half a second in this case.

-   [**from**](/w/index.php?title=svg/attributes/from&action=edit&redlink=1) and [**to**](/w/index.php?title=svg/attributes/to&action=edit&redlink=1) provide the values between which the animation should transition. In this case, it moves the eyeball 50 units to the right.

As it appears above, the animation moves the eyes to the right, then immediately snaps back. There's an attribute called [**fill**](/svg/attributes/fill), which is unfortunately named the same as the [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) property that applies colors and gradients to shapes. Adding a [**fill**](/svg/attributes/fill) attribute here and setting it to **freeze** would keep the eyes looking to the side after the animation ends. But instead, we'll add another animation to return the eyes to their original state:

``` xml
<circle id="eyeball" cx="100" cy="100" r="150" >
    <animate
        id             = "glanceStart"
        attributeType  = "XML"
        attributeName  = "cx"
        begin          = "1s"
        dur            = "0.5s"
        from           = "100"
        to             = "150"
    />
    <animate
        id             = "glanceEnd"
        attributeType  = "XML"
        attributeName  = "cx"
        begin          = "glanceStart.end"
        dur            = "0.5s"
        from           = "150"
        to             = "100"
    />
</circle>
```

 Aside from the inversion of the [**from**](/w/index.php?title=svg/attributes/from&action=edit&redlink=1) and [**to**](/w/index.php?title=svg/attributes/to&action=edit&redlink=1) values, note the *glanceEnd* animation's [**begin**](/w/index.php?title=svg/attributes/begin&action=edit&redlink=1) time is expressed in terms of whenever the previous *glanceStart* animation ends. And notice that in addition to the **xlink:href** and **url()** syntax we've seen used to reference objects, now we see a third form of dot syntax that references the *glanceStart* identifier along with the value of its [**end**](/w/index.php?title=svg/attributes/end&action=edit&redlink=1) attribute.

(See [**SVG animations**](/svg/tutorials/smarter_svg_filters) for details.)

## Blinking

As is true for CSS transitions and animations, you can animate most any numeric or color value. You can also animate complex series of coordinates used in [**path**](/svg/elements/path) definitions, so long as the sequence of path commands match so that there are corresponding sets of points. This allows the eyes to blink. Add this to the *eyelids* object:

``` xml
<path id="eyelids" d="M 200,100 Q 100,200 0,100 Q 100,0 200,100">
    <animate
        id            = "blink"
        attributeType = "XML"
        attributeName = "d"
        from          = "M 200,100 Q 100,200 0,100 Q 100,0 200,100"
        to            = "M 200,100 Q 100,100 0,100 Q 100,100 200,100"
        begin         = "4s; 6s; 8s; 9s; 11.5s; 13s"
        dur           = "0.1s"
    />
</path>
```

 In this case, the [**begin**](/w/index.php?title=svg/attributes/begin&action=edit&redlink=1) attribute specifies half a dozen different values, so the animation executes several times . Between the [**from**](/w/index.php?title=svg/attributes/from&action=edit&redlink=1) and [**to**](/w/index.php?title=svg/attributes/to&action=edit&redlink=1) values, the only values that are modified are the positions of the two control points that affect the shape of the curve, so the animation behaves like this:

![svgGrandTour eyeball blink.png](//static.webplatform.org/7/75/svgGrandTour_eyeball_blink.png)

You can use JavaScript to control these animations more flexibly. To do so, call the **beginElement()** method on the animation object. This example shifts the *x*/*y* coordinates to which the eyes glance, with an optional duration parameter to regulate the speed:

``` js
function glanceTo(x,y,dur) {
    dur = (dur || 0.5) + 's'; // assign 3rd param or default
    var toThere = document.querySelector('#glanceStart');
    var andBack = document.querySelector('#glanceEnd');
    toThere.setAttribute("to", x + " " + y);
    andBack.setAttribute("from", x + " " + y);
    toThere.setAttribute("dur", dur);
    andBack.setAttribute("dur", dur);
    toThere.beginElement();
}
```

 Calling this function keeps the eyes blinking at random points between two and five seconds:

``` js
function blink() {
    var minDelay = 2000;
    var maxExtraDelay = 3000;
    document.querySelector('#blink').beginElement();
    setTimeout(blink, (Math.floor(Math.random() * maxExtraDelay) + minDelay));
}
```

 (See [**SVG animations**](/svg/tutorials/smarter_svg_filters) for details.)

## Interactive Zoom

Suppose you want to click on the graphic to get a closer look at it. Scaling the eyeball would be difficult, because there are now two of them, and they would collide with each other. Instead, you can alter the dimensions of the current [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1) to zoom into the scene.

Links use the same [**a**](/svg/elements/a) element as in HTML, but as usual the **xlink:href** attribute needs its namespace qualified, and it needs to wrap other SVG elements rather than plain text. This link encapsulates the wrapper for both eyes, so clicking on either one activates the link:

``` xml
<a xlink:href="#zoomIn">
  <use xlink:href="#eyes"/>
</a>
<view id="zoomIn" viewBox="100 50 100 100" />
```

 When linking to an internal [**view**](/svg/elements/view) element, its [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1) value overrides that of the [**svg**](/svg/elements/svg) of which it is a descendant, thus zooming the scene:

![svgGrandTour eyeball zoom.png](//static.webplatform.org/thumb/a/ac/svgGrandTour_eyeball_zoom.png/200px-svgGrandTour_eyeball_zoom.png)

The entire eyeball is active by default, but this can be configured. In HTML content, the [**pointer-events**](/css/properties/pointer-events) property allows you to control whether an element's mouse and touch event handlers execute, useful in layered interfaces. SVG allows you to target the active area to the **visibleStroke** or **visibleFill** portion of a graphic (or **visiblePainted** for both). These become active when a graphic's [**visibility**](/css/properties/visibility) is enabled (**visible**), and when [**fill**](/w/index.php?title=svg/properties/fill&action=edit&redlink=1) and [**stroke**](/w/index.php?title=svg/properties/stroke&action=edit&redlink=1) values are defined. (Unlike [**visibility:hidden**](/css/properties/visibility), setting [**display:none**](/css/properties/display) entirely suppresses an element's rendering.)

As in HTML, the [**cursor**](/css/properties/cursor) property allows you to highlight active areas, but unlike HTML, *any* graphic element can be styled separately with the **:hover** pseudoclass, not just links:

``` css
#eyelid:hover, .eyelids:hover { cursor: pointer; }
#eyelid, .eyelids { pointer-events: visiblePainted; }
```

## Animated Zoom

There are two problems with the anchor-zoom navigation described above. First, it only works within SVG files, not inline SVG within HTML. Second, it executes abruptly, the same way anchor navigation scrolls an HTML page.

Both problems can be fixed by overriding the default navigation. First, define alternate [**view**](/svg/elements/view) targets along with an [**animate**](/w/index.php?title=svg/elements/animate&action=edit&redlink=1) element to shift between each target's [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1). Setting [**fill**](/svg/attributes/fill) to **freeze** retains the zoom level after the animation ends:

``` xml
<view id="zoomOut" viewBox="0 0 600 200" />
<view id="zoomIn" viewBox="100 50 100 100" />

<animate
   id            = "zoomNav"
   attributeType = "XML"
   attributeName = "viewBox"
   fill          = "freeze"
   />

<a class="zoom" xlink:href="#zoomIn">
  <use xlink:href="#eyes"/>
</a>
```

 This JavaScript calls **preventDefault()** to disable default navigation for *zoom*-classed links. Instead, it executes the animation modified based on the target's [**viewBox**](/w/index.php?title=svg/attributes/viewBox&action=edit&redlink=1):

``` js
var animate, svg; // corresponds to SVG elements
var duration = '3s';

window.onload = function() {
    svg = document.querySelector('svg');
    animate = document.querySelector('#zoomNav');
    animate.setAttribute('dur', duration);
    animate.setAttribute('from', svg.getAttribute('viewBox'));
    animate.setAttribute('to', svg.getAttribute('viewBox'));
    var links = document.querySelectorAll('a.zoom');
    for (var i = 0, l = links.length; i < l; i++) {
        // replace default navigation:
        links[i].setAttribute('onclick', 'event.preventDefault()');
        links[i].addEventListener('click', zoomNav);
    }
};

function zoomNav(e) {
    var hash = e.currentTarget.getAttribute('xlink:href');
    var tgt = document.querySelector(hash);
    // swap to/from values:
    animate.setAttribute('from', animate.getAttribute('to'));
    animate.setAttribute('to', tgt.getAttribute('viewBox'));
    // execute animation:
    animate.beginElement();
    // apply CSS class to help customize display within each zoom level:
    svg.className = hash.replace(/#/,'');
}
```

 The last line applies different classes to the [**svg**](/svg/elements/svg) container, which we'll use to customize display of the text elements described below for different zoom levels.

## Adding Text

SVG allows you to mix text with other graphics, but these are simple lines of text that do not wrap within a box as in HTML. You ordinarily use **x** and **y** coordinate attributes to position [**text**](/svg/elements/text) elements directly within a graphic. This example relies on SVG's characteristic ability to place text along a curved path:

![svgGrandTour eyeball textRotate.png](//static.webplatform.org/thumb/2/2a/svgGrandTour_eyeball_textRotate.png/200px-svgGrandTour_eyeball_textRotate.png)

The text appears to wrap around a [**circle**](/svg/elements/circle) element, but since circles do not have logical start and end points, you need to use the [rather complex](/svg/tutorials/smarter_svg_shapes) *A* path command to draw two elliptical arc curves, each facing the other, originating and terminating at the left edge:

``` xml
<path id="irisPath" d="M 60,100 A 40,40 0 0 1 140,100 A 40,40 0 0 1 60,100 "/>
<path id="pupilPath" d="M 78,100 A 22,22 0 0 1 122,100 A 22,22 0 0 1 78,100"/>
```

 ![svgGrandTour eyeball textPath.png](//static.webplatform.org/thumb/c/cc/svgGrandTour_eyeball_textPath.png/200px-svgGrandTour_eyeball_textPath.png)

We'll add a reference to a *labels* object along with other eyeball components:

``` xml
<g id="eye">
  <use xlink:href="#eyelids" class="eyelashes" />
  <use xlink:href="#eyelids" class="eyelids"   />
  <use xlink:href="#eyeball" class="eyeball"   />
  <use xlink:href="#labels"/>
</g>
```

 Its [**textPath**](/svg/elements/textPath) diverts a portion of the [**text**](/svg/elements/text) to display along the path:

``` xml
<g id="labels">
  <text>
    <textPath xlink:href="#irisPath"> Iris </textPath>
  </text>
  <text>
    <textPath xlink:href="#pupilPath"> Pupil </textPath>
  </text>
</g>
```

 ![svgGrandTour eyeball text.png](//static.webplatform.org/thumb/d/df/svgGrandTour_eyeball_text.png/200px-svgGrandTour_eyeball_text.png)

Ordinarily, you can increment the [**textPath**](/svg/elements/textPath)'s [**startOffset**](/w/index.php?title=svg/attributes/startOffset&action=edit&redlink=1) attribute in animations to push text along the path. As an alternative in this case, you can use CSS transforms to rotate the circular object:

``` css
#irisPath, #pupilPath {
    fill             : none;
    transform-origin : center         ; -webkit-transform-origin : center  ; -moz-transform-origin : center;
}
#irisPath {
    transform        : rotate(120deg) ; -webkit-transform : rotate(120deg) ; -moz-transform : rotate(120deg);
}
#pupilPath {
    transform        : rotate(20deg)  ; -webkit-transform : rotate(20deg)  ; -moz-transform : rotate(20deg);
}
```

 By default, SVG transforms originate from an element's top-left corner, so to spin the circle properly you need to explicitly set the [**transform-origin**](/css/properties/transform-origin) property to CSS's own default **50% 50%** value. And be careful when mixing transforms, since SVG's get clobbered by CSS's.

![svgGrandTour eyeball textRotate.png](//static.webplatform.org/thumb/2/2a/svgGrandTour_eyeball_textRotate.png/200px-svgGrandTour_eyeball_textRotate.png)

Finally, additional CSS specifies the appearance of the text labels, and displays contextually within the magnified zoom level. Transitions on the [**fill-opacity**](/w/index.php?title=svg/properties/fill-opacity&action=edit&redlink=1) and [**stroke-opacity**](/w/index.php?title=svg/properties/stroke-opacity&action=edit&redlink=1) properties fade them in and out as the zoom animation executes:

``` css
text {
    font-size          : 10px;
    text-transform     : uppercase;
    stroke-width       : 0.5;
    stroke             : black;
    stroke-opacity     : 0;
    fill               : red;
    fill-opacity       : 0;
    /* transition to default zoom level lasts 2 seconds; no delay */
    transition         : all 2s;    -webkit-transition : all 2s;    -moz-transition    : all 2s;
}

svg.zoomIn text {
    fill-opacity       : 0.25;
    stroke-opacity     : 0.25;
    /* transition to magnified zoom level lasts 2 seconds, with 2 second delay */
    transition         : all 2s 2s;    -webkit-transition : all 2s 2s;    -moz-transition    : all 2s 2s;
}
```

 Text letterforms behave just like paths, so the various and fill and stroke properties work the same way as for other shapes.

(See [**SVG text**](/svg/tutorials/smarter_svg_text) for details on text properties.)

Had enough?

![svgGrandTour eyeball tired.png](//static.webplatform.org/thumb/6/69/svgGrandTour_eyeball_tired.png/600px-svgGrandTour_eyeball_tired.png)

## See also

### Related articles

#### Filters

-   [blur()](/css/functions/blur)

-   [brightness()](/css/functions/brightness)

-   [contrast()](/css/functions/contrast)

-   [custom()](/css/functions/custom)

-   [drop-shadow()](/css/functions/drop-shadow)

-   [grayscale()](/css/functions/grayscale)

-   [hue-rotate()](/css/functions/hue-rotate)

-   [invert()](/css/functions/invert)

-   [opacity()](/css/functions/opacity)

-   [saturate()](/css/functions/saturate)

-   [sepia()](/css/functions/sepia)

-   [filter](/css/properties/filter)

-   [feBlend](/svg/elements/feBlend)

-   [feColorMatrix](/svg/elements/feColorMatrix)

-   [feComponentTransfer](/svg/elements/feComponentTransfer)

-   [feComposite](/svg/elements/feComposite)

-   [feConvolveMatrix](/svg/elements/feConvolveMatrix)

-   [feDiffuseLighting](/svg/elements/feDiffuseLighting)

-   [feDisplacementMap](/svg/elements/feDisplacementMap)

-   [feDistantLight](/svg/elements/feDistantLight)

-   [feFlood](/svg/elements/feFlood)

-   [feFuncA](/svg/elements/feFuncA)

-   [feFuncB](/svg/elements/feFuncB)

-   [feFuncG](/svg/elements/feFuncG)

-   [feFuncR](/svg/elements/feFuncR)

-   [feGaussianBlur](/svg/elements/feGaussianBlur)

-   [feImage](/svg/elements/feImage)

-   [feMerge](/svg/elements/feMerge)

-   [feMergeNode](/svg/elements/feMergeNode)

-   [feMorphology](/svg/elements/feMorphology)

-   [feOffset](/svg/elements/feOffset)

-   [fePointLight](/svg/elements/fePointLight)

-   [feSpecularLighting](/svg/elements/feSpecularLighting)

-   [feSpotlight](/svg/elements/feSpotlight)

-   [feTile](/svg/elements/feTile)

-   [feTurbulence](/svg/elements/feTurbulence)

-   [SVG deployment](/svg/tutorials/smarter_svg_deploy)

-   [SVG filters](/svg/tutorials/smarter_svg_filters)

-   [SVG graphic effects](/svg/tutorials/smarter_svg_graphics)

-   **SVG grand tour**

-   [SVG filters](/tutorials/svg_filters)

### Other articles

-   [svg/tutorials/smarter\_svg\_shapes](/svg/tutorials/smarter_svg_shapes) (SVG basic shapes and text)
-   [svg/tutorials/smarter\_svg\_graphics](/svg/tutorials/smarter_svg_graphics) (SVG graphic effects)
-   [svg/tutorials/smarter\_svg\_filters](/svg/tutorials/smarter_svg_filters) (SVG filters)
-   [svg/tutorials/smarter\_svg\_animation](/svg/tutorials/smarter_svg_animation) (SVG animation)
-   [svg/tutorials/smarter\_svg\_deploy](/svg/tutorials/smarter_svg_deploy) (SVG deployment)
