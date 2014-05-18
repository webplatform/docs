{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The rect element is a SVG basic shape to create a rectangle starting with a given with and height beginning at a x- and y-point.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
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
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://www.w3.org/TR/SVG11/shapes.html#RectElement Scalable Vector Graphics: The The ‘rect’ element], Section 9.2

===Attributes===

====Global attributes====
*[[svg/attributes#Conditional_processing_attributes|'''Conditional processing attributes''']]
*[[svg/attributes#Core_attributes|'''Core attributes''']]
*[[svg/attributes#Graphical_event_attributes|'''Graphical events attributes''']]
*[[svg/attributes#Presentation_attributes|'''Presentation attributes''']]

*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.


====Specific attributes====

Specific attributes of '''SVGRectElement''':

*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
*[[svg/properties/rx (SVGRectElement)|'''rx''']]: Gets or sets  the x-axis radius of a rounded corner rectangle.
*[[svg/properties/ry (SVGRectElement)|'''ry''']]: Gets or sets  the y-axis radius of a rounded corner rectangle.

===DOM Interface===

The '''SVGRectElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGRectElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.
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