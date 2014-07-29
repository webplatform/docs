{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Fix multiple broken links
|Checked_Out=No
|High-level issues=Needs Topics
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The rect element is a SVG basic shape to create a rectangle starting with a given with and height beginning at a x- and y-point.}}
{{Markup_Element
|DOM_interface=dom/SVGRectElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following code example,  the rect element is used to draw a purple rectangle.
|Code=<syntaxhighlight lang="xml">
<svg width="200" height="200" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="5" width="100" height="80" fill="purple" />
</svg>

</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/44786e14924371effbe4
}}{{Single Example
|Description=In the following code example, the rect element is used to create a orange rectangle with rounded corners.
|Code=<syntaxhighlight lang="xml">
<svg width="200" height="200" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="5" width="100" height="80" fill="orange" rx="10" ry="10" />
</svg>

</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/9697f0fe090f4ad2e6e9
}}
}}
{{Notes_Section
|Import_Notes====Attributes===

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

*[[svg/attributes/x|'''x''']]
*[[svg/attributes/y|'''y''']]
*[[svg/attributes/width|'''width''']]
*[[svg/attributes/height|'''height''']]
*[[svg/attributes/rx|'''rx''']]
*[[svg/attributes/ry|'''ry''']]

===DOM Interface===

This element implements the [[dom/SVGRectElement|'''SVGRectElement''']] interface.

===Members===

The '''SVGRectElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGRectElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.

The '''SVGRectElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/attributes/fill|'''fill''']]: Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
*[[svg/attributes/fill-opacity|'''fillOpacity''']]: Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
*[[svg/attributes/fill-rule|'''fillRule''']]: Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]: Gets  a value that indicates which element established the current viewport.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/attributes/pointers|'''pointerEvents''']]: Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
*[[svg/properties/requiredExtensions|'''requiredExtensions''']]: Gets a white space-delimited list of required language extensions.
*[[svg/properties/requiredFeatures|'''requiredFeatures''']]: Gets or sets a white space-delimited list of feature strings.
*[[svg/properties/rx (SVGRectElement)|'''rx''']]: Gets or sets  the x-axis radius of a rounded corner rectangle.
*[[svg/properties/ry (SVGRectElement)|'''ry''']]: Gets or sets  the y-axis radius of a rounded corner rectangle.
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
*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=The ‘rect’ element
|URL=http://www.w3.org/TR/SVG11/shapes.html#RectElement
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