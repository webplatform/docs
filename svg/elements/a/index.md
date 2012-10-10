{{Flags
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
|Description=In the following code example, the a element is used to create a hyperlink using the xlink namespace. The link is attached to the circle element inside an inline SVG element.
Copy this sample to a text file and save it with the .html file extension. Run it in Internet Explorer 9 and click on the chocolate circle.

It should look like this:
|LiveURL=
|Code=

&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
	
    &lt;!-- Create an SVG object. --&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
        &lt;!-- Create a link. --&gt;
        &lt;a xlink:href{{=}}"http://msdn.microsoft.com/en-us/ie/"&gt;
          &lt;!-- Create a circle. --&gt;
          &lt;circle cx{{=}}"100" cy{{=}}"100" r{{=}}"50" fill{{=}}"chocolate"/&gt;
          &lt;/circle&gt;										
        &lt;/a&gt;
    &lt;/svg&gt;
		
  &lt;/body&gt;
&lt;/html&gt;	
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
SVG provides an '''a''' element to indicate links (also known as hyperlinks or web links). The '''a''' element may contain any element that its parent may contain, except itself.
SVG uses XLink for all link definitions (that is, <code>xmlns:xlink{{=}}"http://www.w3.org/1999/xlink"</code> must be present in the containing [[svg/elements/svg|'''svg''']] element). Each link associates exactly two resources, one local and one remote, going from the former to the latter.
A link is defined for each separate rendered element contained within the '''a''' element; thus, if the '''a''' element contains three [[svg/elements/circle|'''circle''']] elements, a link is created for each circle. For each rendered element within an '''a''' element, the given rendered element is the local resource (the source anchor for the link).
The remote resource (the destination for the link) is defined by a URL (technically a [http://go.microsoft.com/fwlink/p/?linkid{{=}}203507 W3C IRI]) specified by the XLink (that is, <code>xlink:href</code> attribute) on the '''a''' element. The remote resource may be any web resource (for example, an image, a video clip, a sound bite, a program, another SVG document, an HTML document, an element within the current document, an element within a different document, etc.). By activating these links (by clicking with the mouse, through keyboard input, by voice commands, etc.), users may visit these resources.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199815 Scalable Vector Graphics: Linking], Section 17.4.1


===Members===
The '''SVGAElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''SVGAElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Methods====
The '''SVGAElement''' object has these methods.
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
The '''SVGAElement''' object has these properties.
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
|[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]
|Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/properties/href|'''href''']]
|Gets an <code>xlink:href</code> attribute of an element.
|-
|[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]
|Gets  a value that indicates which element established the current viewport.
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
|[[svg/properties/target|'''target''']]
|Specifies where to open a linked document.
|-
|[[svg/properties/transform|'''transform''']]
|Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
|-
|[[svg/properties/viewportElement|'''viewportElement''']]
|Gets the element that established the current viewport.
|-
|[[svg/properties/xmlbase|'''xmlbase''']]
|Gets or sets the <code>base</code> attribute on the element.
|-
|[[svg/properties/xmllang|'''xmllang''']]
|Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
|-
|[[svg/properties/xmlspace|'''xmlspace''']]
|Gets or sets a value that indicates whether white space is preserved in character data.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}