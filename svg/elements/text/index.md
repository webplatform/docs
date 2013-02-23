{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
|Description=In the following code example, the text element is used to create a text message in olive 36-point Impact type that reads" Internet Explorer Rocks". Copy this sample to a text file and save it with the ''.html'' file extension. Run it in Internet Explorer 9 to see the text.

It should look like this:
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE html>
<html>
    <head></head>
    <body>
        <svg>
            <text x="50" y="50" font-family="Impact" font-size="36" fill="olive">
                SVG Rocks!
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

The XML character data within the '''text''' element, along with relevant attributes and properties and character-to-glyph mapping tables within the font itself, define the glyphs to be rendered. The attributes and properties on the '''text''' element indicate the writing direction, font specification, and painting attributes. These items  describe how  to render characters.

Because  '''text''' elements are rendered by using the same rendering methods as other graphics elements, all of the same coordinate system transformation, painting, clipping, and masking features that apply to shapes (such as paths and rectangles) also apply to '''text''' elements.

You can  apply a gradient, pattern, clipping path, mask, or  filter to text. When  you apply one of these items to text and  you use '''objectBoundingBox'''  to specify a graphical effect relative to the object bounding box, the units for the object bounding box  are computed relative to the entire '''text''' element in all cases, even when different effects are applied to different [[svg/elements/tspan|'''tSpan''']] elements within the same '''text''' element.

The '''text''' element renders its first glyph (after bidirectionality reordering) at the initial current text position, which is established by the [[svg/properties/x|'''x''']] and [[svg/properties/y|'''y''']] attributes on the '''text''' element. (The attributes might be adjusted   because of the value of the '''text-anchor''' property, the presence of a [[svg/elements/textPath|'''textPath''']] element that contains  the first character, or '''x''', '''y''', [[svg/properties/dx|'''dx''']], or [[svg/properties/dy|'''dy''']] attributes on a [[svg/elements/tspan|'''tSpan''']], '''tref''', or '''altGlyph''' element that contains the first character.) After the glyphs that corresponds  to the given character are rendered, the current text position is updated for the next character. In the simplest case, the new current text position is the previous current text position plus the glyphs' advance value (horizontal or vertical).
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.17.3

===Members===

The '''SVGTextElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGTextElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCharNumAtPosition|'''getCharNumAtPosition''']]: Gets the index of the character  that  the glyph cell bounding box contains  at the specified point.
*[[svg/methods/getComputedTextLength|'''getComputedTextLength''']]: Returns the total  sum of all advance values from rendering all characters within the given text element.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getEndPositionOfChar|'''getEndPositionOfChar''']]: Gets the current text position of the specified character after  the character is rendered in the user coordinate system  where  the glyphs that correspond to the specified character are rendered.
*[[svg/methods/getExtentOfChar|'''getExtentOfChar''']]: Gets a  rectangle  that defines the minimum and maximum x-coordinate and y-coordinate values in the user coordinate system where the glyphs that correspond to the specified character are rendered.
*[[svg/methods/getNumberOfChars|'''getNumberOfChars''']]: Gets  the total number of characters that are available for rendering within the current element.
*[[svg/methods/getRotationOfChar|'''getRotationOfChar''']]: Gets the rotation value of the specified character, relative to the current user coordinate system  where  the glyphs that corresponding to the specified character are rendered.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getStartPositionOfChar|'''getStartPositionOfChar''']]: Gets  the current text position of the specified character before the character is rendered in the user coordinate system  where the glyphs that correspond to the specified character are rendered.
*[[svg/methods/getSubStringLength|'''getSubStringLength''']]: Calculates the total sum of all advance values from rendering the specified substring of the characters.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.
*[[svg/methods/selectSubString|'''selectSubString''']]: Selects the specified substring,  just as if  a user selected the substring interactively.

The '''SVGTextElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/attributes/dominant-baseline|'''dominantBaseline''']]: Sets or retrieves a value that determines or redetermines a scaled-baseline table.
*[[svg/properties/dx|'''dx''']]: Gets the [[svg/properties/dx|'''dx''']] attribute on the given element.
*[[svg/properties/dy|'''dy''']]: Gets the  [[svg/properties/dy|'''dy''']]  attribute on the given element.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/attributes/fill|'''fill''']]: Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
*[[svg/attributes/fill-opacity|'''fillOpacity''']]: Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
*[[svg/attributes/fill-rule|'''fillRule''']]: Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/glyph-orientation-horizontal|'''glyphOrientationHorizontal''']]: Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction  of horizontal.
*[[svg/attributes/glyph-orientation-vertical|'''glyphOrientationVertical''']]: Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
*[[svg/attributes/kerning|'''kerning''']]: Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

Gets or sets a value that indicates whether the user-agent should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).
*[[svg/properties/lengthAdjust|'''lengthAdjust''']]: Gets or sets the  [[svg/properties/lengthAdjust|'''lengthAdjust''']] attribute on the given element.
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]: Gets  a value that indicates which element established the current viewport.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/attributes/pointers|'''pointerEvents''']]: Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
*[[svg/properties/requiredExtensions|'''requiredExtensions''']]: Gets a white space-delimited list of required language extensions.
*[[svg/properties/requiredFeatures|'''requiredFeatures''']]: Gets or sets a white space-delimited list of feature strings.
*[[svg/properties/rotate|'''rotate''']]: Gets or sets  the supplemental character rotation about the current text position.
*[[svg/attributes/stroke|'''stroke''']]: Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
*[[svg/attributes/stroke-dasharray|'''strokeDasharray''']]: Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
*[[svg/attributes/stroke-dashoffset|'''strokeDashoffset''']]: Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
*[[svg/attributes/stroke-linecap|'''strokeLinecap''']]: Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
*[[svg/attributes/stroke-linejoin|'''strokeLinejoin''']]: Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
*[[svg/attributes/stroke-miterlimit|'''strokeMiterlimit''']]: Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the [[svg/attributes/stroke-linejoin|'''strokeLinejoin''']] property).
*[[svg/attributes/stroke-opacity|'''strokeOpacity''']]: Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
*[[svg/attributes/stroke-width|'''strokeWidth''']]: Sets or retrieves a value that specifies the width of the stroke on the current object.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/systemLanguage|'''systemLanguage''']]: Gets or sets a comma-separated list of language names.
*[[svg/properties/textLength|'''textLength''']]: Gets or sets the  [[svg/properties/textLength|'''textLength''']] attribute on the given element.
*[[svg/properties/transform|'''transform''']]: Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
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