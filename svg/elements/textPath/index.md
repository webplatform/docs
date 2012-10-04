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
|Description=In the following code example, the '''textPath''' element is used to define a path for text rendering. 
The same path is used in the [[svg/elements/path|'''path''']] example. 
Copy this sample to a text file and save it with the .html file extension. Run it in Internet Explorer 9 to see the text on a path.

It should look like this:
|LiveURL=
|Code=

&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
      &lt;defs&gt;
        &lt;path id{{=}}"myTextPath" d{{=}}"M 50,100 Q 150,50 250,100" /&gt;
      &lt;/defs&gt;
      &lt;text fill{{=}}"steelblue" font-size{{=}}"20"&gt;
        &lt;textPath xlink:href{{=}}"#myTextPath"&gt;Internet Explorer Forever!&lt;/textPath&gt;
      &lt;/text&gt;
    &lt;/svg&gt;
  &lt;/body&gt;
&lt;/html&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
In addition to text  that is drawn in a straight line, you can also  place text along the shape of a [[svg/elements/path|'''path''']] element in SVG. To  render  a block of text  along the shape of a '''path''' element, include the given text within a '''textPath''' element  that  includes an <code>xlink:href</code> attribute with an Internationalized Resource Identifier (IRI) reference to the '''path''' element.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.17.6


===Members===
The '''SVGTextPathElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''SVGTextPathElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Methods====
The '''SVGTextPathElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/getCharNumAtPosition|'''getCharNumAtPosition''']]
|Gets the index of the character  that  the glyph cell bounding box contains  at the specified point.
|-
|[[svg/methods/getComputedTextLength|'''getComputedTextLength''']]
|Returns the total  sum of all advance values from rendering all characters within the given text element.
|-
|[[svg/methods/getEndPositionOfChar|'''getEndPositionOfChar''']]
|Gets the current text position of the specified character after  the character is rendered in the user coordinate system  where  the glyphs that correspond to the specified character are rendered.
|-
|[[svg/methods/getExtentOfChar|'''getExtentOfChar''']]
|Gets a  rectangle  that defines the minimum and maximum x-coordinate and y-coordinate values in the user coordinate system where the glyphs that correspond to the specified character are rendered.
|-
|[[svg/methods/getNumberOfChars|'''getNumberOfChars''']]
|Gets  the total number of characters that are available for rendering within the current element.
|-
|[[svg/methods/getRotationOfChar|'''getRotationOfChar''']]
|Gets the rotation value of the specified character, relative to the current user coordinate system  where  the glyphs that corresponding to the specified character are rendered.
|-
|[[svg/methods/getStartPositionOfChar|'''getStartPositionOfChar''']]
|Gets  the current text position of the specified character before the character is rendered in the user coordinate system  where the glyphs that correspond to the specified character are rendered.
|-
|[[svg/methods/getSubStringLength|'''getSubStringLength''']]
|Calculates the total sum of all advance values from rendering the specified substring of the characters.
|-
|[[svg/methods/hasExtension|'''hasExtension''']]
|Determines if the specified extension  is supported.
|-
|[[svg/methods/selectSubString|'''selectSubString''']]
|Selects the specified substring,  just as if  a user selected the substring interactively.
|}
 

====Properties====
The '''SVGTextPathElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/attributes/baseline-shift|'''baselineShift''']]
|Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.
|-
|[[svg/properties/className|'''className''']]
|Gets  the names of the classes  that are assigned to this object.
|-
|[[svg/attributes/dominant-baseline|'''dominantBaseline''']]
|Sets or retrieves a value that determines or redetermines a scaled-baseline table.
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/attributes/fill|'''fill''']]
|Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
|-
|[[svg/attributes/fill-opacity|'''fillOpacity''']]
|Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
|-
|[[svg/attributes/fill-rule|'''fillRule''']]
|Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/attributes/glyph-orientation-horizontal|'''glyphOrientationHorizontal''']]
|Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction  of horizontal.
|-
|[[svg/attributes/glyph-orientation-vertical|'''glyphOrientationVertical''']]
|Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
|-
|[[svg/properties/href|'''href''']]
|Gets an <code>xlink:href</code> attribute of an element.
|-
|[[svg/attributes/kerning|'''kerning''']]
|Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

Gets or sets a value that indicates whether Metro style app using JavaScript should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).
|-
|[[svg/properties/lengthAdjust|'''lengthAdjust''']]
|Gets or sets the  [[svg/properties/lengthAdjust|'''lengthAdjust''']] attribute on the given element.
|-
|'''method'''
|Gets the '''method''' attribute on the given '''textPath''' element.
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
|[[svg/properties/spacing|'''spacing''']]
|Gets  the    [[svg/properties/spacing|'''spacing''']]  attribute on the given  '''textPath'''  element.
|-
|[[svg/properties/startOffset|'''startOffset''']]
|Gets the  [[svg/properties/startOffset|'''startOffset''']]  attribute on the given  '''textPath'''  element.
|-
|[[svg/attributes/stroke|'''stroke''']]
|Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
|-
|[[svg/attributes/stroke-dasharray|'''strokeDasharray''']]
|Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
|-
|[[svg/attributes/stroke-dashoffset|'''strokeDashoffset''']]
|Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
|-
|[[svg/attributes/stroke-linecap|'''strokeLinecap''']]
|Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
|-
|[[svg/attributes/stroke-linejoin|'''strokeLinejoin''']]
|Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
|-
|[[svg/attributes/stroke-miterlimit|'''strokeMiterlimit''']]
|Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the [[svg/attributes/stroke-linejoin|'''strokeLinejoin''']] property).
|-
|[[svg/attributes/stroke-opacity|'''strokeOpacity''']]
|Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
|-
|[[svg/attributes/stroke-width|'''strokeWidth''']]
|Sets or retrieves a value that specifies the width of the stroke on the current object.
|-
|[[svg/properties/style|'''style''']]
|Gets a [[css/cssom/style|'''style''']] object.
|-
|[[svg/properties/systemLanguage|'''systemLanguage''']]
|Gets or sets a comma-separated list of language names.
|-
|[[svg/properties/textLength|'''textLength''']]
|Gets or sets the  [[svg/properties/textLength|'''textLength''']] attribute on the given element.
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