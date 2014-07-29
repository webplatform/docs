{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
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
|Description=In the following code example, the '''textPath''' element is used to define a path for text rendering.
The same path is used in the [[svg/elements/path|'''path''']] example.
Copy this sample to a text file and save it with the ''.html'' file extension. Run it in Internet Explorer 9 to see the text on a path.

It should look like this:
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <defs>
        <path id="myTextPath" d="M 50,100 Q 150,50 250,100" />
      </defs>
      <text fill="steelblue" font-size="20">
        <textPath xlink:href="#myTextPath">Internet Explorer Forever!</textPath>
      </text>
    </svg>
  </body>
</html>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

In addition to text  that is drawn in a straight line, you can also  place text along the shape of a [[svg/elements/path|'''path''']] element in SVG. To  render  a block of text  along the shape of a '''path''' element, include the given text within a '''textPath''' element  that  includes an '''xlink:href''' attribute with an Internationalized Resource Identifier (IRI) reference to the '''path''' element.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.17.6

===Members===

The '''SVGTextPathElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGTextPathElement''' object has these methods:

*[[svg/methods/getCharNumAtPosition|'''getCharNumAtPosition''']]: Gets the index of the character  that  the glyph cell bounding box contains  at the specified point.
*[[svg/methods/getComputedTextLength|'''getComputedTextLength''']]: Returns the total  sum of all advance values from rendering all characters within the given text element.
*[[svg/methods/getEndPositionOfChar|'''getEndPositionOfChar''']]: Gets the current text position of the specified character after  the character is rendered in the user coordinate system  where  the glyphs that correspond to the specified character are rendered.
*[[svg/methods/getExtentOfChar|'''getExtentOfChar''']]: Gets a  rectangle  that defines the minimum and maximum x-coordinate and y-coordinate values in the user coordinate system where the glyphs that correspond to the specified character are rendered.
*[[svg/methods/getNumberOfChars|'''getNumberOfChars''']]: Gets  the total number of characters that are available for rendering within the current element.
*[[svg/methods/getRotationOfChar|'''getRotationOfChar''']]: Gets the rotation value of the specified character, relative to the current user coordinate system  where  the glyphs that corresponding to the specified character are rendered.
*[[svg/methods/getStartPositionOfChar|'''getStartPositionOfChar''']]: Gets  the current text position of the specified character before the character is rendered in the user coordinate system  where the glyphs that correspond to the specified character are rendered.
*[[svg/methods/getSubStringLength|'''getSubStringLength''']]: Calculates the total sum of all advance values from rendering the specified substring of the characters.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.
*[[svg/methods/selectSubString|'''selectSubString''']]: Selects the specified substring,  just as if  a user selected the substring interactively.

The '''SVGTextPathElement''' object has these properties:

*[[svg/attributes/baseline-shift|'''baselineShift''']]: Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.
*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/attributes/dominant-baseline|'''dominantBaseline''']]: Sets or retrieves a value that determines or redetermines a scaled-baseline table.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/attributes/fill|'''fill''']]: Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
*[[svg/attributes/fill-opacity|'''fillOpacity''']]: Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
*[[svg/attributes/fill-rule|'''fillRule''']]: Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/glyph-orientation-horizontal|'''glyphOrientationHorizontal''']]: Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction  of horizontal.
*[[svg/attributes/glyph-orientation-vertical|'''glyphOrientationVertical''']]: Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
*[[svg/properties/href|'''href''']]: Gets an '''xlink:href''' attribute of an element.
*[[svg/attributes/kerning|'''kerning''']]: Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

Gets or sets a value that indicates whether Metro style app using JavaScript should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).
*[[svg/properties/lengthAdjust|'''lengthAdjust''']]: Gets or sets the  [[svg/properties/lengthAdjust|'''lengthAdjust''']] attribute on the given element.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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