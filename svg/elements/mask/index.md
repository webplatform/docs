{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=In the following code example, an alpha mask is used to filter text. A linear gradient is defined that runs from magenta to cyan. A mask is then defined that will use the gradient to filter defined text. Alpha masking uses the image brightness to define the opacity of the final image. Magenta is less "bright" than cyan, so the resulting masked image will be less opaque on the left and more opaque on the right.
Copy this sample to a text file and save it with the .html file extension. Run it in Internet Explorer 9 to see the alpha-masked text.

The masked text will look like this:
|LiveURL=
|Code=

&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
      &lt;defs&gt;
        &lt;!-- Define linear gradient for magenta to cyan. --&gt;
        &lt;linearGradient id{{=}}"magenta2cyan" &gt;
          &lt;!-- First color is magenta. --&gt;
          &lt;stop offset{{=}}"0%" style{{=}}"stop-color:magenta"/&gt;
          &lt;!-- Second color is cyan. --&gt;
          &lt;stop offset{{=}}"100%" style{{=}}"stop-color:cyan"/&gt;
        &lt;/linearGradient&gt;
        &lt;!-- Define mask. --&gt;
        &lt;mask id{{=}}"myMask" 
						x{{=}}"0" y{{=}}"0" width{{=}}"400" height{{=}}"400"&gt;
          &lt;rect x{{=}}"0" y{{=}}"0" width{{=}}"400" height{{=}}"400"
						fill{{=}}"url(#magenta2cyan)" /&gt;
        &lt;/mask&gt;
        &lt;!-- Define text. --&gt;
        &lt;text id{{=}}"myText" x{{=}}"50" y{{=}}"50" 
					font-family{{=}}"Verdana" font-size{{=}}"32"  &gt;
				SVG forever!
        &lt;/text&gt;
      &lt;/defs&gt;		
      &lt;!-- Use text with mask and gradient. --&gt;
      &lt;use xlink:href{{=}}"#myText" fill{{=}}"navy" mask{{=}}"url(#myMask)" /&gt;
    &lt;/svg&gt;
		
  &lt;/body&gt;
&lt;/html&gt;
	
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
In SVG, you can use  any graphical object or [[svg/elements/g|'''g''']] element  as an alpha mask for compositing that object into the background.
You can define a mask by using a '''mask''' element. You can use or reference a mask by using the <code>mask</code> attribute within an appropriate element (for example, <code>&lt;rect  mask{{=}}"url(#myMask)"/&gt;</code>). A '''mask''' element can contain any graphical elements or container elements, such as a [[svg/elements/g|'''g''']] element.
The <code>mask</code> attribute cannot reference a non-existent object, and the referenced object must be a '''mask''' element.
The effect is the same as if the child elements of the '''mask''' element are rendered into an off-screen image  that  has been initialized to transparent black. Any graphical object that uses or references the given '''mask''' element is painted onto the background through the mask, which completely or partially masks  parts of the graphical object.
For any graphical object that is used as a mask, the mask value at any point is computed from the color channel values and alpha channel value as follows:
#Compute a linear luminance value from the color channel values. For example, convert the original image color values (potentially in the sRGB color space) to the linear RGB color space. Then, by using non-premultiplied linear RGB color values, apply the luminance-to-alpha coefficients to convert the linear RGB color values to linear luminance values.
#If the graphics object also includes an alpha channel,  multiply the computed linear luminance value by the corresponding alpha value to produce the mask value.

For a four-channel RGBA graphics object that is used as a mask, both the color channels and the alpha channel of the mask contribute to the masking operation. The alpha mask that is used to composite the current object into the background represents the product of the luminance of the color channels and the alpha channel from the mask.
For a three-channel RGB graphics object that is used as a mask (for example, when you reference  a 3-channel image file), the effect is the same as if the object is converted into a 4-channel RGBA image with the alpha channel uniformly set to 1.
For a single-channel image that is used as a mask (for example, when you reference a 1-channel grayscale image file), the effect is the same as if the object  is converted into a 4-channel RGBA image, where the single channel from the referenced object is used to compute the three color channels and the alpha channel is uniformly set to 1.
'''Note'''  When  you reference  a grayscale image file, you must consider the transfer curve that relates the encoded grayscale values to linear light values  when you compute the color channels.
The effect of a mask is the same as  if there  is  no mask, but  the alpha channel of the given object is multiplied  by the mask's resulting alpha values (that is, the product of the mask's luminance from its color channels multiplied by the mask's alpha channel).
'''Note'''  The paths, shapes (for example, circle), and text in SVG are all treated as four-channel RGBA images for the purposes of masking operations.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199810 Scalable Vector Graphics: Clipping, Masking and Compositing], Section 14.6.2


===Members===
The '''SVGMaskElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''SVGMaskElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Methods====
The '''SVGMaskElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/hasExtension|'''hasExtension''']]
|Determines if the specified extension  is supported.
|}
 

====Properties====
The '''SVGMaskElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/className|'''className''']]
|Gets  the names of the classes  that are assigned to this object.
|-
|[[svg/properties/clipPath|'''clipPath''']]
|Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/attributes/mask|'''mask''']]
|Sets or retrieves a value that indicates a SVG mask.
|-
|[[svg/properties/maskContentUnits|'''maskContentUnits''']]
|Gets the [[svg/properties/maskContentUnits|'''maskContentUnits''']] attribute of the '''mask''' element.
|-
|[[svg/properties/maskUnits|'''maskUnits''']]
|Gets  the [[svg/properties/maskUnits|'''maskUnits''']] attribute of the  '''mask'''  element.
|-
|[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]
|Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
|-
|[[svg/properties/requiredExtensions|'''requiredExtensions''']]
|Gets a white space-delimited list of required language extensions.
|-
|[[svg/properties/requiredFeatures|'''requiredFeatures''']]
|Gets or sets a white space-delimited list of feature strings.
|-
|[[svg/properties/style|'''style''']]
|Gets a [[css/cssom/style|'''style''']] object.
|-
|[[svg/properties/systemLanguage|'''systemLanguage''']]
|Gets or sets a comma-separated list of language names.
|-
|[[svg/properties/viewportElement|'''viewportElement''']]
|Gets the element that established the current viewport.
|-
|[[svg/properties/width|'''width''']]
|Defines the width of an element.
|-
|[[svg/properties/x|'''x''']]
|Gets or sets the x-coordinate value.
|-
|[[svg/properties/xmlbase|'''xmlbase''']]
|Gets or sets the <code>base</code> attribute on the element.
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
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}