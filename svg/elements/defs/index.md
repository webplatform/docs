{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs properly flagged and automatically collected children instead of manual links, summary, spec reference, standardization status
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
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

See the [[svg/elements/use|'''use''']] element for an example of using it with the '''defs''' element.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.4

===Members===

The '''SVGDefsElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGDefsElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.

The '''SVGDefsElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]: Gets  a value that indicates which element established the current viewport.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/requiredExtensions|'''requiredExtensions''']]: Gets a white space-delimited list of required language extensions.
*[[svg/properties/requiredFeatures|'''requiredFeatures''']]: Gets or sets a white space-delimited list of feature strings.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/systemLanguage|'''systemLanguage''']]: Gets or sets a comma-separated list of language names.
*[[svg/properties/transform|'''transform''']]: Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.
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