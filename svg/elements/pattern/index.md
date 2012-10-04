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
|Description=In the following code example, a pattern fills a circle. The pattern is made up of a repeated series of wedge-shaped paths.
Copy this sample to a text file and save it with the .html file extension. Run it in Internet Explorer 9 to see the pattern-filled circle.

The pattern-filled circle will look like this:
|LiveURL=
|Code=

&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
    &lt;!-- Create SVG container. --&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
      &lt;!-- Definitions --&gt;
      &lt;defs&gt;
        &lt;!-- Define pattern for fill. --&gt;
        &lt;pattern id{{=}}"myPattern" patternUnits{{=}}"userSpaceOnUse"
						x{{=}}"0" y{{=}}"0" width{{=}}"30" height{{=}}"30" &gt;
          &lt;!-- Create path for individual piece of pattern. --&gt;
          &lt;path d{{=}}"M 0 10 L 25 30 L 50 30 Z" stroke{{=}}"darkorchid" 
						stroke-width{{=}}"3" fill{{=}}"cornflowerblue" /&gt;
        &lt;/pattern&gt;			
      &lt;/defs&gt;
			
      &lt;!-- Circle that will use pattern definition for fill. --&gt;
      &lt;circle cx{{=}}"100" cy{{=}}"100" r{{=}}"75" stroke{{=}}"forestgreen"
				stroke-width{{=}}"3" fill{{=}}"url(#myPattern)" /&gt;
    &lt;/svg&gt;
  &lt;/body&gt;
&lt;/html&gt;
	
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
You can use a pattern  to fill or stroke an object by using a predefined graphic object  that is  replicated (that is, tiled) at fixed intervals along the x-axis  and y-axis  to cover the areas to be painted.  You can define a pattern by  using a '''pattern''' element.  You can then reference the pattern by  the  <code>fill</code> and <code>stroke</code>  properties on a given graphics element to specify  that the given element  is  filled or stroked with the referenced pattern.
The  [[svg/properties/x|'''x''']], [[svg/properties/y|'''y''']], [[svg/properties/width|'''width''']], [[svg/properties/height|'''height''']], and [[svg/properties/patternUnits|'''patternUnits''']]  attributes define a reference rectangle somewhere on the infinite SVG canvas. The reference rectangle has its upper-left corner  at ('''x''', '''y''') and its lower-right corner  at ('''x''' + '''width''', '''y''' + '''height'''). The tiling theoretically extends a series of such rectangles to infinity along the x-axis (positive) and y-axis (negative), with rectangles starting at ('''x''' + ''m''·'''width''', y + ''n''·'''height''') for each possible ''m'' and ''n'' integer value.
For more information, see [http://go.microsoft.com/fwlink/p/?linkid{{=}}203737 Scalable Vector Graphics (SVG) 1.0 Specification].
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.5


===Members===
The '''SVGPatternElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''SVGPatternElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Methods====
The '''SVGPatternElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/hasExtension|'''hasExtension''']]
|Determines if the specified extension  is supported.
|}
 

====Properties====
The '''SVGPatternElement''' object has these properties.
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
|[[svg/properties/href|'''href''']]
|Gets an <code>xlink:href</code> attribute of an element.
|-
|[[svg/attributes/mask|'''mask''']]
|Sets or retrieves a value that indicates a SVG mask.
|-
|[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]
|Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
|-
|[[svg/properties/patternContentUnits|'''patternContentUnits''']]
|Gets or sets the [[svg/properties/patternContentUnits|'''patternContentUnits''']] property on the given '''pattern''' element, defining the coordinate system for the contents of the '''pattern''' element.
|-
|[[svg/properties/patternTransform|'''patternTransform''']]
|Gets or sets the definition of an optional transformation from the pattern 
coordinate system onto the target coordinate system.
|-
|[[svg/properties/patternUnits|'''patternUnits''']]
|Gets or sets the [[svg/properties/patternUnits|'''patternUnits''']] property on the given '''pattern''' element, defining the coordinate system for attributes [[svg/properties/x|'''x''']], [[svg/properties/y|'''y''']], [[svg/properties/width|'''width''']] and [[svg/properties/height|'''height''']].
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