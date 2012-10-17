{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following code example, the clipPath element is used to create a clipping path that will visually hide part of an element. The clipping path is defined by a circle in a defs element and has a defined URL.

The original path would have looked like this:

<syntaxhighlight lang="xml">
<path d="M 50,100 Q 150,50 250,100" stroke="hotpink" 
    stroke-width="10" fill="white"/>
</syntaxhighlight>
|Code=&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
			
      &lt;path d{{=}}"M 50,100 Q 150,50 250,100" stroke{{=}}"hotpink" 
          stroke-width{{=}}"10" fill{{=}}"white" /&gt;
    &lt;/svg&gt;
		
  &lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=HTML
|Description=The path after being clipped by the circle looks like this:

<syntaxhighlight lang="xml">

    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
		
      &lt;defs&gt;
        &lt;clipPath id{{=}}"myClipPath"&gt;
          &lt;circle cx{{=}}100 cy{{=}}100 r{{=}}50 /&gt;
        &lt;/clipPath&gt;
      &lt;/defs&gt;
			
      &lt;path d{{=}}"M 50,100 Q 150,50 250,100" stroke{{=}}"hotpink" 
          stroke-width{{=}}"10" fill{{=}}"white" clip-path{{=}}"url(#myClipPath)"/&gt;
    &lt;/svg&gt;
</syntaxhighlight>
|Code=&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
		
      &lt;defs&gt;
        &lt;clipPath id{{=}}"myClipPath"&gt;
          &lt;circle cx{{=}}100 cy{{=}}100 r{{=}}50 /&gt;
        &lt;/clipPath&gt;
      &lt;/defs&gt;
			
			  &lt;path d{{=}}"M 50,100 Q 150,50 250,100" stroke{{=}}"hotpink" 
			  stroke-width{{=}}"10" fill{{=}}"white" clip-path{{=}}"url(#myClipPath)"/&gt;
    &lt;/svg&gt;
		
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199810 Scalable Vector Graphics: Clipping, Masking and Compositing], Section 14.6.1


===Members===
The '''SVGClipPathElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''SVGClipPathElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Methods====
The '''SVGClipPathElement''' object has these methods.
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
The '''SVGClipPathElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/className|'''className''']]
|Gets  the names of the classes  that are assigned to this object.
|-
|[[svg/properties/clipPathUnits|'''clipPathUnits''']]
|Gets or sets the  given '''SVGClipPathElement''' element.
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
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
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