{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Needed, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|SVG filter effects apply graphics operations such as blurs and color transformations to a source graphic. Filters may be applied to presentational SVG elements as well as to grouping elements like <g>. The <code>filter</code> element specifies the position, dimensions, resolution and units for a filter effect. <code>filter</code> elements typically have multiple child elements to specify filter primitives that combine together to create the final graphics effect.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGFilterElement
|Content=An SVG filter applies a graphics effect to an SVG element. In SVG 1.1, the range of available graphics effects includes blurs, convolutions, color curve manipulation, cross-component color transfers, erosion effects, blending, compositing and more.  The <code>filter</code> element declares a filter effect and is usually included in the <code>defs</code> section of an SVG XML document. The filter element contains a set of child elements that specify the individual graphics operations or "filter primitives" that comprise that filter operation. Filter effects are applied to an SVG element by adding a <code>filter</code> property, set to the id of the desired filter element. 

Below is a basic example of an SVG Filter that shows a gaussian blur applied to an SVG rectangle element. In this example, we first declare a filter whose id is'gblur". Within this filter element, we declare a filter primitive [feGausssianBlur] with a standard deviation of 5. After closing our tags, we draw a rectangle with the SVG <code>rect</code> element.  We apply the blur filter to it, by adding a filter property that references it.

<syntaxhighlight lang="xml">
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
</syntaxhighlight>

[[Image:BasicSVGFilterExampleGaussBlur.png|alt=image showing input and output of a blur filter effect]]

===Filter Region===
The <code>filter</code> element may optionally define the position, dimensions, resolution, and units for the output of a filter effect. The position and dimensions of a filter may be specified using the following properties: x, y, width, height. The default values for these properties are *not intuitive* and are:

* x: -10%
* y: -10%
*width: 120%
*height: 120%

This has the effect that, by default, the output of a filter paints onto the screen with a 10% overflow all around relative to the input element. In some cases (such as blur effects) this may be desirable. In other cases, such as lighting effects, this may be undesirable, and the filter region should be specified explicitly. The below example shows the effect of specifying a filter effects region with x and y set at 50%: the filter effects region effectively clips the output.

<syntaxhighlight lang="xml" highlight="4">
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
</syntaxhighlight>


[[Image:BasicSVGFilterExampleWithClipRegion.png|alt=image showing the result of specifying a custom filter effects region]]

===Filter Resolution===
By default, it's left up to the browser to decide what resolution to use when performing operations on filter inputs, but it's possible to explicitly define a resolution for the browser to use. Choosing a filter resolution significantly lower than the display default will result in visible pixelation but filters will probably execute faster. Choosing a filter resolution significantly higher than the display default can cause slow filter performance. Filter resolution may be separately specified in both the [[svg/properties/filterResX|X]] and [[svg/properties/filterResY|Y]] dimension.

Below we show an example of blurs with low values of FilterRes. The first example shows a filterRes with a single value which is applied to both the X and Y dimensions. The second example shows a filterRes with two values, which results in a low resolution blur in just the Y dimension.

<syntaxhighlight lang="xml">
<svg width="450px" height="300px" viewbox="0 0 450 300"
     xmlns="http://www.w3.org/2000/svg" version="1.1">
   <title>Example showing filterRes</title>
      <defs>
        <filter id="lowresblur" filterRes="25" x="-50%" y="-50%" width="200%" height="200%">
           <feGaussianBlur stdDeviation="5"/>
       </filter>
          
        <filter id="lowresblurY" filterRes="450 25" x="-50%" y="-50%" width="200%" height="200%">
           <feGaussianBlur stdDeviation="5"/>
        </filter>
      </defs>


<rect x="25" y="50" width="100" height="100" fill="blue" stroke="red"/>         

<rect x="175" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#lowresblur)"/>
         
<rect x="325" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#lowresblurY)"/>

</svg>​
</syntaxhighlight>

[[Image:SVGFiltersFilterResExample.png|alt=image showing the result of specifying a custom filter effects region]]

===Units for Filter Effects===
filterUnits
By default, the unit system that specify the filter effects region (x,y,width,height) for the filter element is relative to the dimensions of the element referencing the filter, or in SVG terms the "objectBoundingBox". When we write <code>x="50%"</code> it means "set the starting x position of the filter region to 50% of the rectangle element we're filtering". But you may specify the units to be used explicitly by setting the <code>filterUnits</code> property. The two alternatives are "objectBoundingBox" (the default which we're just described) or "userSpaceOnUse". userSpaceOnUse sets the filter units and the coordinate system to the canvas of the referencing element, or in SVG terms, the "userSpaceOnUse".

primitiveUnits
In addition to the unit system for the filter itself, you may also specify the unit system that the child filter primitives will use. Once again, the choice is between userSpaceOnUse and objectBoundingBox. These effect the coordinates and the values for the filter primitives.

In the example below, we set the unit systems of both the filter and filter primitives to the four combinations possible for userSpaceOnUse and objectBoundingBox, while achieving the same filter effect. In this example, we use an <code><feFlood></code> primitive to generate a rectangular color field that is offset from its referencing element then we use <code><feMerge></code> to combine it with the original element (the <code>SourceGraphic</code>. 

<syntaxhighlight lang="xml">
<svg width="600px" height="300px" viewbox="0 0 600 300"
     xmlns="http://www.w3.org/2000/svg" version="1.1">

<title>A basic filter example</title>
   <defs>
       
     <filter filterUnits="objectBoundingBox" primitiveUnits="objectBoundingBox" id="BoxBox" x="0%%" y="0%" width="100%" height="100%">
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
</syntaxhighlight>

Note: that when we use <code>userSpaceOnUse</code>, we have to calculate our filter and feFlood coordinates offset from the (0,0) of the user space that the <code><rect></code> has been drawn on. 

[[Image:SVGFilterUnitsExamples.png|alt=image showing four identical filters with different unit systems for filterUnits and primitiveUnits]]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=Basic filter effect example
|Code=<svg width="200px" height="200px" viewbox="0 0 200 200"
     xmlns="http://www.w3.org/2000/svg" version="1.1">

<title>A basic filter example</title>
   <defs>
     <filter id="gblur">
        <feGaussianBlur stdDeviation="5"/>
     </filter>
   </defs>

<rect x="50" y="50" width="100" height="100" fill="blue" stroke="red" filter="url(#gblur)"/>

</svg>​​​​​​​​​​​
|LiveURL=http://jsfiddle.net/jsfmullany/djQ9A/
}}
}}
{{Notes_Section
|Usage=Within the enclosing filter element, a filter effect is defined by taking inputs, applying transformation operations and feeding the results of those transformations into further operations. Advanced filters typically contain 10 or more individual filter elements in an input/output chain.

If no other input is specified, but one is required, the first filter primitive within a filter will will take a rasterized (bitmapped) version of the referring element as its input. Subequent filter primitives that expect an input will take the output of the immediately preceding filter primitive as input. 

In complex filters, it can become difficult to keep track (and debug) inputs and outputs if they are left implicit; and it's good practice to explicitly declare inputs and outputs for each primitive.

SVG filter primitives can be divided into inputs, transformations, lighting effects and combinations.

Inputs:
* feFlood: generates a color field
* feTubulence: generates a wide variety of noise effects
* feImage: generates an image from an external image reference

Transformations:
*feColorMatrix: transforms the input values of an RBGA pixel into output values
*feComponentTransfer: adjusts the color curve of an individual color channel
*feConvolveMatrix: replaces each pixel with a new pixel calculated from pixel values in an area around the current pixel (that includes the current pixel)
*feGaussianBlur: replaces the current pixel with a weighted average of pixels in an area around the pixel
*feDisplacementMap: moves each pixel from its current position based on the R,G or B values from another image.
*feMorphology: replaces each pixel with a new pixel calculated from the maximum value of all pixels in an area around that pixel.
*feOffset: moves the input from its current position

Lighting Effects:
*feSpecularLighting: provides a "shiny" 2D or pseudo-3D lighting effect
*feDiffuseLighting: provides a "matte" 2D or pseudo-3D lighting effect
*feDistantLight: provides a distant light source for specular or diffuse lighting
*feSpotLight: provides a conic light source for specular or diffuse lighting
*fePointLight: provides a point light source for specular or diffuse lighting

Combinations:
feMerge: provides a simple composite of intermediate filter results
feBlend: blends multiple inputs using color rules
feComposite: blends multiple inputs using alpha values
feTile: tiles input to output a pattern
|Notes====Remarks===
Although SVG is a vector graphics technology, it's important to emphasize that SVG Filters perform *pixel-level* operations on all inputs (including SVG shapes) and produce rasterized (bitmapped) outputs at a specified level of resolution. Applying a 10x scale transform (for example) on an plain SVG curve that has been filtered at normal screen resolution will produce pixelated edges since the anti-aliasing of the original graphic has been converted to pixels by the filter and scaled up.

Remember that you're writing XML when you're writing filters, so *don't forget to close all those tags* or omit required properties or the filter won't execute at all.

A filter element is never rendered directly. It is only referenced using the filter property on the element to which the filter is applied. Note that the [[css/properties/display|'''display''']] property does not apply to the <code>filter</code> element and  elements are not directly rendered even if the '''display''' property is set to a value other than "none".   Conversely, <code>filter</code> elements are available for referencing even when the'''display''' property on the <code>filter</code>element or any of its ancestors is set to "none".

It is currently (Fall 2012) contemplated that in the future, SVG filters can be referenced via a [[CSS Filter]] and used to apply advanced effects to HTML elements.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.1


===Members===
The '''SVGFilterElement''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''SVGFilterElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/setFilterRes|'''setFilterRes''']]
|Sets the X and Y values of the [[svg/properties/filterResX|'''filterRes''']] attribute.
|}
 

====Properties====
The '''SVGFilterElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/className|'''className''']]
|Gets  the names of the classes  that are assigned to this object.
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/properties/filter|'''filter''']]
|The [[svg/properties/filter|'''filter''']] property is generally used to apply a previously define '''filter''' to an applicable element.
|-
|[[svg/properties/filterResX|'''filterResX''']]
|Corresponds to the X component of the attribute filterRes on the given filter element.
|-
|[[svg/properties/filterResY|'''filterResY''']]
|Corresponds to the Y component of the attribute filterRes on the given filter element.
|-
|[[svg/properties/filterUnits|'''filterUnits''']]
|Defines the coordinate system for the filter attributes.
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/properties/primitiveUnits|'''primitiveUnits''']]
|Specifies the coordinate system for the various length values within the filter primitives and for the attributes that define the filter primitive subregion. The filter primitives identify a subregion which restricts calculation and rendering of the given filter primitive. The default filter primitive subregion is equal to the filter region.
|-
|[[svg/properties/style|'''style''']]
|Gets a [[css/cssom/style|'''style''']] object.
|-
|[[svg/properties/width|'''width''']]
|Defines the width of an element.
|-
|[[svg/properties/x|'''x''']]
|Gets or sets the x-coordinate value.
|-
|[[svg/properties/xmllang|'''xmllang''']]
|Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
|-
|[[svg/properties/xmlspace|'''xmlspace''']]
|Gets or sets a value that indicates whether white space is preserved in character data.
|-
|[[svg/properties/y|'''y''']]
|Gets or sets the y-coordinate value.
|}
 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=SVG 1.1 (Second Edition)
|URL=www.w3.org/TR/SVG/
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=<filter>
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=<filter>
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=RIM OS2
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=IE10
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=iOS 6
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}