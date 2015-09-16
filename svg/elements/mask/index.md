---
title: mask
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, usage, spec reference,  standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/mask

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, an alpha mask is used to filter text. A linear gradient is defined that runs from magenta to cyan. A mask is then defined that will use the gradient to filter defined text. Alpha masking uses the image brightness to define the opacity of the final image. Magenta is less "bright" than cyan, so the resulting masked image will be less opaque on the left and more opaque on the right.

Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the alpha-masked text.

The masked text will look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <defs>
        <!-- Define linear gradient for magenta to cyan. -->
        <linearGradient id="magenta2cyan" >
          <!-- First color is magenta. -->
          <stop offset="0%" style="stop-color:magenta"/>
          <!-- Second color is cyan. -->
          <stop offset="100%" style="stop-color:cyan"/>
        </linearGradient>
        <!-- Define mask. -->
        <mask id="myMask" x="0" y="0" width="400" height="400">
          <rect x="0" y="0" width="400" height="400" fill="url(#magenta2cyan)" />
        </mask>
        <!-- Define text. -->
        <text id="myText" x="50" y="50" font-family="Verdana" font-size="32"  >
         SVG forever!
        </text>
      </defs>
      <!-- Use text with mask and gradient. -->
      <use xlink:href="#myText" fill="navy" mask="url(#myMask)" />
    </svg>
  </body>
</html>
```

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

In SVG, you can use any graphical object or [**g**](/svg/elements/g) element as an alpha mask for compositing that object into the background.

You can define a mask by using a **mask** element. You can use or reference a mask by using the **mask** attribute within an appropriate element (for example, **\<rect mask="url(\#myMask)"/\>**). A **mask** element can contain any graphical elements or container elements, such as a [**g**](/svg/elements/g) element.

The **mask** attribute cannot reference a non-existent object, and the referenced object must be a **mask** element.

The effect is the same as if the child elements of the **mask** element are rendered into an off-screen image that has been initialized to transparent black. Any graphical object that uses or references the given **mask** element is painted onto the background through the mask, which completely or partially masks parts of the graphical object.

For any graphical object that is used as a mask, the mask value at any point is computed from the color channel values and alpha channel value as follows:

1.  Compute a linear luminance value from the color channel values. For example, convert the original image color values (potentially in the sRGB color space) to the linear RGB color space. Then, by using non-premultiplied linear RGB color values, apply the luminance-to-alpha coefficients to convert the linear RGB color values to linear luminance values.
2.  If the graphics object also includes an alpha channel, multiply the computed linear luminance value by the corresponding alpha value to produce the mask value.

For a four-channel RGBA graphics object that is used as a mask, both the color channels and the alpha channel of the mask contribute to the masking operation. The alpha mask that is used to composite the current object into the background represents the product of the luminance of the color channels and the alpha channel from the mask.

For a three-channel RGB graphics object that is used as a mask (for example, when you reference a 3-channel image file), the effect is the same as if the object is converted into a 4-channel RGBA image with the alpha channel uniformly set to 1.

For a single-channel image that is used as a mask (for example, when you reference a 1-channel grayscale image file), the effect is the same as if the object is converted into a 4-channel RGBA image, where the single channel from the referenced object is used to compute the three color channels and the alpha channel is uniformly set to 1.

**Note:** When you reference a grayscale image file, you must consider the transfer curve that relates the encoded grayscale values to linear light values when you compute the color channels.

The effect of a mask is the same as if there is no mask, but the alpha channel of the given object is multiplied by the mask's resulting alpha values (that is, the product of the mask's luminance from its color channels multiplied by the mask's alpha channel).

**Note:** The paths, shapes (for example, circle), and text in SVG are all treated as four-channel RGBA images for the purposes of masking operations.

### Standards information

-   [Scalable Vector Graphics: Clipping, Masking and Compositing](http://go.microsoft.com/fwlink/p/?linkid=199810), Section 14.6.2

### Members

The **SVGMaskElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGMaskElement** object has these methods:

-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGMaskElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**maskContentUnits**](/svg/properties/maskContentUnits): Gets the [**maskContentUnits**](/svg/properties/maskContentUnits) attribute of the **mask** element.
-   [**maskUnits**](/svg/properties/maskUnits): Gets the [**maskUnits**](/svg/properties/maskUnits) attribute of the **mask** element.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
