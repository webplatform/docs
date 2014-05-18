{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The line element creates a line segment interconnecting two points.}}
{{Markup_Element
|DOM_interface=dom/SVGLineElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=In the following code example, the line element is used to draw a salmon-colored line.
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1 Basic//EN" 	"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11-basic.dtd">
<svg width="400" height="400">
  <line x1="50" y1="50" x2="150" y2="150" stroke="salmon" stroke-width="10" />
</svg>
</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/9e2c858dc34a018a483d018a483d
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://www.w3.org/TR/SVG11/shapes.html#LineElement Scalable Vector Graphics: Basic Shapes], Section 9.5

===Attributes===

====Global attributes====
*[[svg/attributes#Conditional_Processing_Attributes|'''Conditional processing attributes''']]
*[[svg/attributes#Core_Attributes|'''Core attributes''']]
*[[svg/attributes#Graphical_Event_Attributes|'''Graphical events attributes''']]
*[[svg/attributes#Presentation_Attributes|'''Presentation attributes''']]

*[[svg/attributes/style|'''style''']]
*[[svg/attributes/class|'''class''']]
*[[svg/attributes/externalResourcesRequired|'''externalResourcesRequired''']]
*[[svg/attributes/transform|'''transform''']]

====Specific attributes====

Specific attributes of '''SVGRectElement''':

*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
*[[svg/properties/rx (SVGRectElement)|'''rx''']]: Gets or sets  the x-axis radius of a rounded corner rectangle.
*[[svg/properties/ry (SVGRectElement)|'''ry''']]: Gets or sets  the y-axis radius of a rounded corner rectangle.

===DOM Interface===

The '''SVGLineElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGLineElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.

The '''SVGLineElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/attributes/fill|'''fill''']]: Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
*[[svg/attributes/fill-opacity|'''fillOpacity''']]: Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
*[[svg/attributes/fill-rule|'''fillRule''']]: Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/marker|'''marker''']]: Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given [[svg/elements/path|'''path''']] element or basic shape.
*[[svg/attributes/marker-end|'''markerEnd''']]: Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given [[svg/elements/path|'''path''']] element or basic shape.
*[[svg/attributes/marker-mid|'''markerMid''']]: Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given [[svg/elements/path|'''path''']] element or basic shape.
*[[svg/attributes/marker-start|'''markerStart''']]: Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given [[svg/elements/path|'''path''']] element or basic shape.
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
*[[svg/properties/x1 (SVGLineElement)|'''x1''']]: Gets or sets the x-coordinate for the start of a line.
*[[svg/properties/x2 (SVGLineElement)|'''x2''']]: Gets or sets the x-coordinate for the end of a line.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.
*[[svg/properties/y1 (SVGLineElement)|'''y1''']]: Gets or sets the y-coordinate for the start of a line.
*[[svg/properties/y2 (SVGLineElement)|'''y2''']]: Gets or sets the y-coordinate for the end of a line.
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