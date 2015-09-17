---
title: 'filter'
code_samples:
  - 'http://jsfiddle.net/jsfmullany/djQ9A/'
compatibility:
  feature: filter
  topic: svg
notes:
  - 'Fix broken links'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGFilterElement](/w/index.php?title=svg/objects/SVGFilterElement&action=edit&redlink=1)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'SVG filter effects apply graphics operations such as blurs and color transformations to a source graphic. Filters may be applied to graphical SVG elements (&lt;circle&gt;, &lt;text&gt;) as well as to grouping elements (&lt;g&gt;). The filter element specifies the position, dimensions, resolution and units for a filter effect. filter elements typically have multiple child elements (filter primitives) that combine together to create the final graphics effect.'
tags:
  - Markup_Elements
  - Graphics
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/objects/SVGFilterElement
    - feFlood
    - feMerge
    - 'CSS Filter'
uri: svg/elements/filter

---
## Summary

SVG filter effects apply graphics operations such as blurs and color transformations to a source graphic. Filters may be applied to graphical SVG elements (&lt;circle&gt;, &lt;text&gt;) as well as to grouping elements (&lt;g&gt;). The filter element specifies the position, dimensions, resolution and units for a filter effect. filter elements typically have multiple child elements (filter primitives) that combine together to create the final graphics effect.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGFilterElement](/w/index.php?title=svg/objects/SVGFilterElement&action=edit&redlink=1)

An SVG filter applies a graphics effect to an SVG element. In SVG 1.1, the range of available graphics effects includes blurs, convolutions, color curve manipulation, cross-channel color effects, erosion effects, blending, compositing and more. The **filter** element declares a filter effect and is usually included in the **defs** section of an SVG XML document or within an inline SVG element in a HTML5 document. The filter element contains a set of child elements that specify the individual graphics operations or "filter primitives" that comprise that filter operation. Filter effects are applied to an SVG element by adding a **filter** property, set to the id of the desired filter element.

Below is a basic example of an SVG Filter that shows a gaussian blur applied to an SVG rectangle element. In this example, we first declare a filter whose id is "gblur". Within this filter element, we declare a filter primitive (**feGausssianBlur**) with a standard deviation of 5. After closing our tags, we draw a rectangle with the SVG **rect** element. We apply the filter to the element by adding a filter property that references its id, **gblur**.

``` xml
<svg width="200px" height="200px" viewbox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" version="1.1">
<title>A basic filter example</title>
   <defs>
     <filter id="gblur">
        <feGaussianBlur stdDeviation="5"/>
     </filter>
   </defs>
<rect x="25" y="50" width="100" height="100" fill="blue" stroke="red"/>
<rect x="175" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#gblur)"/>
</svg>​​​​​​​​​​​
```

 ![image showing input and output of a blur filter effect](/assets/public/6/6b/BasicSVGFilterExampleGaussBlur.png)

### Filter Region

The **filter** element may optionally define the position, dimensions, resolution, and units for the output of a filter effect. The position and dimensions of a filter may be specified using the following parameters: x, y, width, height. The default values are \*not intuitive\* and are:

-   x: -10%
-   y: -10%
-   width: 120%
-   height: 120%

This has the effect that, by default, the output of a filter paints onto the screen with a 10% overflow all around relative to the input element. In some cases (such as blur effects) this may be desirable. In other cases, such as lighting effects, this may be undesirable, and the filter region should be specified explicitly. The below example shows the effect of specifying a filter effects region with x and y set at 50%: the filter effects region effectively clips the output.

``` xml
<svg width="200px" height="200px" viewbox="0 0 200 200 xmlns="http://www.w3.org/2000/svg" version="1.1">
<title>An example of a clipped filter region</title>
   <defs>
     <filter id="gblurclipped" x="50%" y="50%" width="60%" height="60%">
        <feGaussianBlur stdDeviation="5"/>
     </filter>
   </defs>
<rect x="25" y="50" width="100" height="100" fill="blue" stroke="red"/>
<rect x="175" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#gblurclipped)"/>
</svg>​​​​​​​​​​​
```

 ![image showing the result of specifying a custom filter effects region](/assets/public/4/46/BasicSVGFilterExampleWithClipRegion.png)

### Filter Resolution

By default, the browser decides what resolution to use when performing operations on filter inputs, but it is possible to set this resolution by explicitly setting the **filterRes** property. Choosing a filter resolution significantly lower than the display default will result in visible pixelation but filters will execute faster. Choosing a filter resolution significantly higher than the default will cause slow filter performance. Filter resolution may be separately specified in both the [**X**](/svg/properties/filterResX) and [**Y**](/svg/properties/filterResY) dimension.

Below we show an example of blurs with low values of filterRes. The first example shows a filterRes with a single low value which is applied to both the X and Y dimensions. The second example shows a filterRes with two values - a high value for X and a low value for the Y dimension - which results in a low resolution blur in just the Y dimension. Setting a very low resolution results in visible pixelation.

``` xml
<svg width="450px" height="300px" viewbox="0 0 450 300" xmlns="http://www.w3.org/2000/svg" version="1.1">
   <title>Example showing filterRes</title>
      <defs>
        <filter id="lowresblur" filterRes="25" x="-50%" y="-50%" width="200%" height="200%">
           <feGaussianBlur stdDeviation="5"/>
       </filter>
        <filter id="lowresblurY" filterRes="425 25" x="-50%" y="-50%" width="200%" height="200%">
           <feGaussianBlur stdDeviation="5"/>
        </filter>
      </defs>
<rect x="25" y="50" width="100" height="100" fill="blue" stroke="red"/>
<rect x="175" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#lowresblur)"/>
<rect x="325" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#lowresblurY)"/>
</svg>​
```

 ![image showing the result of specifying a custom filter effects region](/assets/public/b/bf/SVGFiltersFilterResExample.png)

### Units and Coordinates for Filter Effects

#### filterUnits

By default, the units and coordinate system for the filter effects region (x,y,width,height) of a filter element are set relative to the bounding box of the element referencing the filter. In SVG terms, this is called the "objectBoundingBox". When we write **x="50%"** it means "set the starting x position of the filter region at the left side of the bounding box of the referencing element + 50% of the width of the element".

But you may also specify the units and coordinates explicitly by setting the **filterUnits** property. The two alternatives are "objectBoundingBox" (the default which we're just described) or "userSpaceOnUse". userSpaceOnUse sets the filter units and the coordinate system to the canvas of the referencing element, or in SVG terms, the "userSpaceOnUse".

#### primitiveUnits

In addition to the unit system for the filter itself, you may also specify the unit system that the filter's child filter primitives will use. Once again, the choice is between userSpaceOnUse and objectBoundingBox. These affect the 0,0 coordinates and the unit values for the filter primitives in the same way as for filterUnits.

In the example below, we set the unit systems of both the filter and filter primitives to the four combinations possible for userSpaceOnUse and objectBoundingBox, while achieving the same filter effect. Here, we use an **\<[feFlood](/w/index.php?title=feFlood&action=edit&redlink=1)\>** primitive to generate a rectangular color field that is offset from its referencing element. Then we use **\<[feMerge](/w/index.php?title=feMerge&action=edit&redlink=1)\>** to combine the feFlood with the original element (the **SourceGraphic**).

``` xml
<svg width="600px" height="300px" viewbox="0 0 600 300" xmlns="http://www.w3.org/2000/svg" version="1.1">
<title>A basic filter example</title>
   <defs>
     <filter filterUnits="objectBoundingBox" primitiveUnits="objectBoundingBox" id="BoxBox" x="0%" y="0%" width="100%" height="100%">
        <feFlood x="20%" y="20%" width="50%" height="50%" flood-color="green" result="greenbox"/>
        <feMerge>
            <feMergeNode in="SourceGraphic"/>
            <feMergeNode in="greenbox"/>
         </feMerge>
     </filter>
     <filter filterUnits="userSpaceOnUse" primitiveUnits="objectBoundingBox" id="UserBox" x="175" y="50" width="120" height="120">
        <feFlood x="20%" y="20%" width="50%" height="50%" flood-color="green" result="greenbox"/>
        <feMerge>
            <feMergeNode in="SourceGraphic"/>
            <feMergeNode in="greenbox"/>
         </feMerge>
     </filter>
     <filter filterUnits="objectBoundingBox" primitiveUnits="userSpaceOnUse" id="BoxUser" x="0%" y="0%" width="100%" height="100%">
        <feFlood x="349" y="74" width="60" height="60" flood-color="green" result="greenbox"/>
        <feMerge>
            <feMergeNode in="SourceGraphic"/>
            <feMergeNode in="greenbox"/>
         </feMerge>
     </filter>
     <filter filterUnits="userSpaceOnUse" primitiveUnits="userSpaceOnUse" id="UserUser" x="475" y="50" width="120" height="120">
        <feFlood x="499" y="74" width="60" height="60" flood-color="green" result="greenbox"/>
        <feMerge>
            <feMergeNode in="SourceGraphic"/>
            <feMergeNode in="greenbox"/>
         </feMerge>
     </filter>
   </defs>
<rect x="25" y="50" width="120" height="120" fill="blue" stroke="red" filter="url(#BoxBox)"/>
<rect x="175" y="50" width="120" height="120" fill="red" stroke="blue" filter="url(#UserBox)"/>
<rect x="325" y="50" width="120" height="120" fill="grey" stroke="black" filter="url(#BoxUser)"/>
<rect x="475" y="50" width="120" height="120" fill="black" stroke="purple" filter="url(#UserUser)"/>
</svg>​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​​
```

 Note: that when we use **userSpaceOnUse**, we calculate our filter and feFlood coordinates offset from the (0,0) of the user space that the **\<rect\>** has been drawn on, using viewbox units.

![image showing four identical filters with different unit systems for filterUnits and primitiveUnits](/assets/public/0/03/SVGFilterUnitsExamples.png)

## Examples

Basic filter effect example

```


<svg width="200px" height="200px" viewbox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" version="1.1">
<title>A basic filter example</title>
   <defs>
     <filter id="gblur">
        <feGaussianBlur stdDeviation="5"/>
     </filter>
   </defs>
<rect x="50" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#gblur)"/>
</svg>​​​​​​​​​​​
```

</pre>
[View live example](http://jsfiddle.net/jsfmullany/djQ9A/)

## Usage

     Within the enclosing filter element, a filter effect is defined by taking inputs, applying transformation operations and feeding the results of those transformations into further operations. Advanced filters typically can contain 5or more individual filter primitives in an input/output chain. Filters are also capable of inheriting from other filters via the xlink:href attribute, however, this is not widely supported in current browsers (Dec 2012).

Most filter attributes are animateable via the \<animate\> element (available in all browses except IE as of November 2012). With the increasing prevalence of GPU acceleration of filters, performance on many browsers is now acceptable.

Child elements of the Filter element - filter primitives - have two optional attributes that specify the color space within which color interpolation calculations are performed: **color-interpolation** and **color-interpolation-filters**. The default for the former is sRGB, and the default for the latter is linearRGB. Manipulations that invert the color space (through feColorMatrix or feComponentTransfer) can result in "non-intuitive" results. For example, a color inversion of a greyscale image in linearRGB will result in a pronounced shift toward whiter tones. This can be corrected by setting the value of the primitive to sRGB. These attributes can be set on the individual filter primitives or inherited from the filter element itself.

If no other input is specified, but one is required, the first filter primitive within a filter will take a rasterized (bitmapped) version of the referring element as its input. Subsequent filter primitives that expect an input will take the result of the immediately preceding filter primitive as input.

In complex filters, it can become difficult to keep track (and debug) inputs and outputs if they are left implicit; and it is good practice to explicitly declare inputs and outputs for each primitive.

SVG filter primitives can be colloquially divided into inputs, transformations, lighting effects and combinations.

Inputs:

-   feFlood: generates a color field
-   feTurbulence: generates a wide variety of noise effects
-   feImage: generates an image from an external image reference (or object reference, but this is not widely supported in current browsers Dec '12)

Transformations:

-   feColorMatrix: transforms the input values of an RBGA pixel into output values
-   feComponentTransfer: adjusts the color curve of an individual color channel
-   feConvolveMatrix: replaces each pixel with a new pixel calculated from pixel values in an area relative to the the current pixel)
-   feGaussianBlur: replaces the current pixel with a weighted average of pixels in an area around the pixel
-   feDisplacementMap: moves each pixel from its current position based on the R,G or B values from another input graphic.
-   feMorphology: replaces each pixel with a new pixel calculated from the maximum or minimum value of all pixels in a rectangular area around that pixel.
-   feOffset: moves the input from its current position

Lighting Effects:

-   feSpecularLighting: provides a "shiny" 2D or pseudo-3D lighting effect
-   feDiffuseLighting: provides a "matte" 2D or pseudo-3D lighting effect
-   feDistantLight: provides a distant light source for specular or diffuse lighting
-   feSpotLight: provides a conic section light source for specular or diffuse lighting
-   fePointLight: provides a point light source for specular or diffuse lighting

Combinations:

-   feMerge: creates a simple **over** composite from multiple inputs (including previous filter inputs)
-   feBlend: blends multiple inputs using mixing rules
-   feComposite: combines multiple inputs using set combination rules, taking into account alpha values.
-   feTile: tiles input to create a repeating pattern

## Notes

### Remarks

Although SVG is a vector graphics technology, it is important to emphasize that SVG Filters perform \*pixel-level\* operations on all inputs (including SVG shapes) and produce rasterized (bitmapped) outputs at a specified level of resolution. Applying a 10x scale transform (for example) on an plain SVG curve that has been filtered at normal screen resolution will produce pixelated edges since the anti-aliasing of the original graphic has been converted to pixels by the filter and scaled up. (It is unclear whether this is spec compliant or just a limitation of current implementations)

Remember that SVG is XML when you write filters, so all tags must be closed and many properties and attributes are required to be specified explicitly or the filter will not execute.

A filter element is never rendered directly. It is only referenced using the filter property on the element to which the filter is applied. Note that the [**display**](/css/properties/display) property does not apply to the **filter** element and elements are not directly rendered even if the **display** property is set to a value other than "none". Conversely, **filter** elements are available for referencing even when the**display** property on the **filter**element or any of its ancestors is set to "none".

SVG filters can be referenced via a [CSS Filter](/w/index.php?title=CSS_Filter&action=edit&redlink=1), although as of November 2013, only a subset of primitives are supported via this mechanism.

### Syntax

### Standards information

-   <http://www.w3.org/TR/SVG/filters.html#FilterElement>

### Members

#### Methods

The **SVGFilterElement** object has these methods.

-   [**setFilterRes**](/svg/methods/setFilterRes): Sets the X and Y values of the [**filterRes**](/svg/properties/filterResX) attribute.

#### Properties

The **SVGFilterElement** object has these properties.

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**filter**](/svg/properties/filter): The [**filter**](/svg/properties/filter) property is generally used to apply a previously defined **filter** to an applicable element.
-   [**filterResX**](/svg/properties/filterResX): Corresponds to the X component of the attribute filterRes on the given filter element.
-   [**filterResY**](/svg/properties/filterResY): Corresponds to the Y component of the attribute filterRes on the given filter element.
-   [**filterUnits**](/svg/properties/filterUnits): Defines the coordinate system for the filter attributes.
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**primitiveUnits**](/svg/properties/primitiveUnits): Specifies the coordinate system for the various length values within the filter primitives and for the attributes that define the filter primitive subregion. The filter primitives identify a subregion which restricts calculation and rendering of the given filter primitive. The default filter primitive subregion is equal to the filter region.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## Related specifications

[SVG 1.1 (Second Edition)](http://www.w3.org/TR/SVG/)
:   W3C Recommendation

## See also

### Related articles

#### Visual Effects

-   [color](/css/color)

-   [Colors by Hue](/css/color/colors_by_hue)

-   [Colors by Name](/css/color/colors_by_name)

-   [Colors by Saturation](/css/color/colors_by_saturation)

-   [User-Defined System Colors](/css/color/user-defined_system_colors)

-   [-ms-high-contrast](/css/high_contrast_mode/properties/-ms-high-contrast)

-   [ms-high-contrast-adjust](/css/high_contrast_modeapis/properties/ms-high-contrast-adjust)

-   [-ms-progress-appearance](/css/properties/-ms-progress-appearance)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [clip](/css/properties/clip)

-   [cursor](/css/properties/cursor)

-   [opacity](/css/properties/opacity)

-   [zoom](/css/properties/zoom)

-   [height](/html/attributes/height)

-   [blink](/html/elements/blink)

-   **filter**

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### External resources

SVG Filter Effects <http://www.w3.org/TR/SVG/filters.html#FilterElement>
