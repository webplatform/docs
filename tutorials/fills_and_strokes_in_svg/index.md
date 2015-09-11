---
title: Fills and strokes in SVG
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Fills_and_Strokes)'
notes:
  - 'Fix broken links'
readiness: 'Almost Ready'
summary: 'This article shows how to add fills and strokes to the SVG shapes you have drawn.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'SVG specification'
    - 'normal XML-stylesheet syntax'
uri: 'tutorials/fills and strokes in svg'

---
## <span>Summary</span>

This article shows how to add fills and strokes to the SVG shapes you have drawn.

So now with your knowledge of how to draw all sorts of shapes, your next goal is probably coloring them in. There are several ways to do this, including specifying attributes on the object, using inline CSS, using an embedded CSS section, or using an external CSS file. Most SVG you'll find around the web uses inline CSS, but there are advantages and disadvantages for all the types.

## <span>Fill and Stroke Attributes</span>

### <span>Painting</span>

It's been a bit difficult to avoid putting some of this in your face up until now, but in case you haven't noticed, most basic coloring can be done by setting two attributes on the node: `fill` and `stroke`. Fill sets the color inside the object and stroke sets the color of the line drawn around the object. You can use the same css color naming schemes that you use in HTML, whether that's color names (that is *red*), rgb values (that is *rgb(255,0,0)*), hex values, rgba values, etc.

     <rect x="10" y="10" width="100" height="100" stroke="blue" fill="purple"
           fill-opacity="0.5" stroke-opacity="0.8"/>

In addition, you can specify the opacity of either the fill or stroke separately in SVG. These are controlled by the `fill-opacity` and `stroke-opacity` attributes.

     Note, in Firefox 3+ rgba values are also allowed, and will give the same effect, but for compatibility with other viewers, its often best to specify the fill/stroke opacity separately. If you specify both an rgba value and a fill/stroke opacity value, both will be applied.

### <span>Stroke</span>

In addition to just its color properties, there are a few other attributes available to control the way a stroke is drawn on a line.

 ![SVG Stroke Linecap Example.png](/assets/public/2/28/SVG_Stroke_Linecap_Example.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="160" height="140" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <line x1="40" x2="120" y1="20" y2="20" stroke="black" stroke-width="20" stroke-linecap="butt"/>
      <line x1="40" x2="120" y1="60" y2="60" stroke="black" stroke-width="20" stroke-linecap="square"/>
      <line x1="40" x2="120" y1="100" y2="100" stroke="black" stroke-width="20" stroke-linecap="round"/>
    </svg>

Before I discuss these, I just want to note that strokes are drawn so that they are centered around the path, that is, in the example above the path is shown in pink, and the stroke in black. The `stroke-width` property defines the width of this stroke. As you can see the stroke is distributed evenly on both sides of the path.

The second of these is the `stroke-linecap` property, demoed above. This controls the shape shown at the end of lines. There are three possible values for it. `butt` closes the line off with a straight edge that's normal (at 90 degrees to) the direction of the stroke and crosses its end. `square` has essentially the same appearance, but stretches the stroke slightly beyond the actual path. The distance that the stroke goes beyond the path is controlled by the `stroke-width` property. `round` produces a rounded effect on the end of the stroke, The radius of this curve is, again, controlled by the stroke width.

There is also a property, `stroke-linejoin` to control how the line is drawn at the joint between two line segments.

 ![SVG Stroke Linejoin Example.png](/assets/public/a/ad/SVG_Stroke_Linejoin_Example.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="160" height="280" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <polyline points="40 60 80 20 120 60" stroke="black" stroke-width="20"
          stroke-linecap="butt" fill="none" stroke-linejoin="miter"/>

      <polyline points="40 140 80 100 120 140" stroke="black" stroke-width="20"
          stroke-linecap="round" fill="none" stroke-linejoin="round"/>

      <polyline points="40 220 80 180 120 220" stroke="black" stroke-width="20"
          stroke-linecap="square" fill="none" stroke-linejoin="bevel"/>
    </svg>

Each of these polylines have two segments. The joint where the two meet is controlled by the `stroke-linejoin` attribute. There are three possible values for this attribute. `miter` will extend the line slightly beyond its normal width to create a square corner where only one angle is used. `round`, again draws a rounded line segment. `bevel` will create a new angle to aid in the transition between the two segments.

Finally, you can also use dashed line types on a stroke, by specifying the `stroke-dasharray` attribute.

![SVG Stroke Dasharray Example.png](/assets/public/4/4a/SVG_Stroke_Dasharray_Example.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="200" height="150" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <path d="M 10 75 Q 50 10 100 75 T 190 75" stroke="black"
        stroke-linecap="round" stroke-dasharray="5,10,5" fill="none"/>
      <path d="M 10 75 L 190 75" stroke="red"
        stroke-linecap="round" stroke-width="1" stroke-dasharray="5,5" fill="none"/>
    </svg>

The `stroke-dasharray` attribute takes as an argument a series of comma separated numbers. Note, unlike paths these numbers *must* be comma separated. You can insert whitespace, too, if you want, but the numbers must have commas in between them. Each of the numbers specifies a distance for first the filled area, and then for the unfilled area. So in the above example, the second path fills 5 pixel units, then leaves 5 blank, then fills 5 again. You can specify more numbers if you would like a more complicated dash pattern. The first example specifies three numbers, in which case the renderer loops the numbers twice to create an even pattern. So the first path renders 5 filled, 10 empty, 5 filled, and then loops back to create 5 empty, 10 filled, 5 empty. The pattern then loops again.

There are a few additional stroke and fill properties available, including `fill-rule` which specifies how to color in shapes that overlap themselves, `stroke-miterlimit` which deals with a stroke should draw miters and when it shouldn't, and `stroke-dashoffset` which specifies where to start a dasharray on a line.

## <span>Using CSS</span>

In addition to setting attributes on objects, you can also use CSS to style fills and strokes on them. The syntax for this is the same as CSS used in normal HTML, except you'll be setting values like `fill` and `stroke` instead of `background-color` or `border`. I should note that not all attributes can be set via CSS. Things that deal with painting and filling are usually available, so `fill`, `stroke`, `stroke-dasharray`, etc. can all be set this way, in addition to the gradient and pattern versions of those shown below. Things like `width`, `height`, or path commands, `d`, can't be set through CSS. Its easiest just to test and find out what is available and what isn't.

The [SVG specification](/w/index.php?title=SVG_specification&action=edit&redlink=1) decides strictly between attributes, that are *properties* and other attributes. The former can be modified with CSS, the latter not. CSS can be inserted inline with the element via the style attribute:

    <rect x="10" height="180" y="10" width="180" style="stroke: black; fill: red;"/>

or can be moved to a special style section that you include. Instead of shoving such a section into a `<head>` like you do in HTML though, its included in an area called [[\<defs\>]]. `<defs>` stands for definitions, and its here where you can create elements that don't appear in the SVG directly, but are used by other elements.

    <?xml version="1.0" standalone="no"?>
    <svg width="200" height="200" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <defs>
        <style type="text/css"><![CDATA[
           #MyRect {
             stroke: black;
             fill: red;
           }
        ]]></style>
      </defs>
      <rect x="10" height="180" y="10" width="180" id="MyRect"/>
    </svg>

Moving styles to an area like this can make it easier to adjust properties on large groups of elements. You can also use things like the **hover pseudo classes** to create rollover effects:

    #MyRect:hover {
       stroke: black;
       fill: blue;
    }

The list could go on and on, but you're better off reading a CSS tutorial to learn about it. Some things that work in normal HTML won't work, like the `before` and `after` pseudo classes, so a bit of experimentation is needed to sort everything out.

You can also specify an external style sheet for your CSS rules through [normal XML-stylesheet syntax](/w/index.php?title=normal_XML-stylesheet_syntax&action=edit&redlink=1):

    <?xml version="1.0" standalone="no"?>
    <?xml-stylesheet type="text/css" href="style.css"?>

    <svg width="200" height="150" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <rect height="10" width="10" id="MyRect"/>
    </svg>

where style.css looks something like:

    #MyRect {
      fill: red;
      stroke: black;
    }