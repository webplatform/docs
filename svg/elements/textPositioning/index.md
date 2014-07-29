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
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.17.2

===Members===

The '''SVGTextPositioningElement''' object has these methods:

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

The '''SVGTextPositioningElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/dx|'''dx''']]: Gets the [[svg/properties/dx|'''dx''']] attribute on the given element.
*[[svg/properties/dy|'''dy''']]: Gets the  [[svg/properties/dy|'''dy''']]  attribute on the given element.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/lengthAdjust|'''lengthAdjust''']]: Gets or sets the  [[svg/properties/lengthAdjust|'''lengthAdjust''']] attribute on the given element.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/requiredExtensions|'''requiredExtensions''']]: Gets a white space-delimited list of required language extensions.
*[[svg/properties/requiredFeatures|'''requiredFeatures''']]: Gets or sets a white space-delimited list of feature strings.
*[[svg/properties/rotate|'''rotate''']]: Gets or sets  the supplemental character rotation about the current text position.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/systemLanguage|'''systemLanguage''']]: Gets or sets a comma-separated list of language names.
*[[svg/properties/textLength|'''textLength''']]: Gets or sets the  [[svg/properties/textLength|'''textLength''']] attribute on the given element.
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