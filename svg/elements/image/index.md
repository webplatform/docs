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
|Description=In the following code example, two images are displayed on the screen. They are the same image but the size and position are determined by the attributes of the image element.
Copy this sample to a text file and save it with the .html file extension. Run it in Internet Explorer 9 to see the two images on the screeen.

The images will look like this:
|LiveURL=
|Code=

&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
	
    &lt;!-- Create an SVG object. --&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
      &lt;!-- Load an image. --&gt;			
      &lt;image x{{=}}"50" y{{=}}"50" width{{=}}"100" height{{=}}"100"
				xlink:href{{=}}"svg.png"/&gt;	
      &lt;image x{{=}}"150" y{{=}}"150" width{{=}}"50" height{{=}}"50"
				xlink:href{{=}}"svg.png"/&gt;					
    &lt;/svg&gt;
		
  &lt;/body&gt;
&lt;/html&gt;
	
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.11


===Members===
The '''SVGImageElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''SVGImageElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Methods====
The '''SVGImageElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/getBBox|'''getBBox''']]
|Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
|-
|[[svg/methods/getCTM|'''getCTM''']]
|Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
|-
|[[svg/methods/getScreenCTM|'''getScreenCTM''']]
|Gets  the transformation matrix from the current user units to the screen coordinate system.
|-
|[[svg/methods/getTransformToElement|'''getTransformToElement''']]
|Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
|-
|[[svg/methods/hasExtension|'''hasExtension''']]
|Determines if the specified extension  is supported.
|}
 

====Properties====
The '''SVGImageElement''' object has these properties.
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
|[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]
|Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/properties/href|'''href''']]
|Gets an <code>xlink:href</code> attribute of an element.
|-
|[[svg/attributes/mask|'''mask''']]
|Sets or retrieves a value that indicates a SVG mask.
|-
|[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]
|Gets  a value that indicates which element established the current viewport.
|-
|[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]
|Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
|-
|[[svg/attributes/pointers|'''pointerEvents''']]
|Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
|-
|[[svg/properties/preserveAspectRatio|'''preserveAspectRatio''']]
|Gets  an XML value that indicates whether to force uniform graphic scaling.
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
|[[svg/properties/transform|'''transform''']]
|Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
|-
|[[svg/properties/viewBox|'''viewBox''']]
|Gets  a value that indicates how a graphic scales to fit a container element.
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