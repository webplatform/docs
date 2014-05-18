{{Page_Title|circle}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The circle element is an SVG basic shape, used to create circles based on a center point and a radius.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following code example, the circle element is used to draw a tomato-colored circle with radius 50.
|Code=<syntaxhighlight lang="xml">
<svg width="400" height="400">
  <circle cx="100" cy="100" r="50" fill="tomato" />
</svg>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The arc of a '''circle''' element begins at the 3 o'clock point on the radius and progresses towards the 9 o'clock point. The starting point and direction of the arc are affected by the user space transform in the same manner as the geometry of the element.
|Import_Notes====Standards information===

*[http://www.w3.org/TR/SVG11/shapes.html#InterfaceSVGCircleElement Scalable Vector Graphics: Basic Shapes], Section 9.8.2

===Members===

Specific attributes of '''SVGCircleElement''':

*[[svg/properties/cx|'''cx''']]: Gets or sets  the x-coordinate of the center of a circle or an ellipse.
*[[svg/properties/cy|'''cy''']]: Gets or sets  the y-coordinate of the center of a circle or an ellipse.
*[[svg/properties/r|'''r''']]: Gets or sets the radius of a circle.

Global attributes of '''SVGCircleElement''':

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/attributes/fill|'''fill''']]: Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
*[[svg/attributes/fill-opacity|'''fillOpacity''']]: Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
*[[svg/attributes/fill-rule|'''fillRule''']]: Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]: Gets  a value that indicates which element established the current viewport.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/attributes/pointers|'''pointerEvents''']]: Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
*[[svg/properties/requiredExtensions|'''requiredExtensions''']]: Gets a white space-delimited list of required language extensions.
*[[svg/properties/requiredFeatures|'''requiredFeatures''']]: Gets or sets a white space-delimited list of feature strings.
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
*[[svg/properties/transform|'''transform''']]: Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.

The '''SVGCircleElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGCircleElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=SVG 1.1
|URL=http://www.w3.org/TR/SVG/shapes.html#CircleElement
|Status=W3C Recommendation
}}
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