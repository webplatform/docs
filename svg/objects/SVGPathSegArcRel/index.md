{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
|High-level issues=Stub
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=

===Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The '''a''' command uses relative coordinates to draw an elliptical arc from the current point to (x, y). The size and orientation of the ellipse are defined by two radius values ([[svg/properties/rx (SVGEllipseElement)|'''rx''']], [[svg/properties/ry (SVGEllipseElement)|'''ry''']]) and a rotation about the x-axis, which indicates how the ellipse is rotated relative to the current coordinate system. The center ([[svg/properties/cx|'''cx''']], [[svg/properties/cy|'''cy''']]) of the ellipse is calculated automatically to meet the constraints  from  the other parameters. large-arc-flag and sweep-flag contribute to the automatic calculations and help determine how the arc is drawn.

|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204736 Scalable Vector Graphics: Paths], Section 8.5.12

===Members===

The '''SVGPathSegArcRel''' object has these properties:

*[[svg/properties/angle|'''angle''']]: Gets or sets  a value that indicates an angle unit.
*[[svg/properties/largeArcFlag|'''largeArcFlag''']]: Gets or sets  the value of the large-arc-flag parameter.
*[[svg/properties/pathSegType|'''pathSegType''']]: Gets the type of the path segment.
*[[svg/properties/pathSegTypeAsLetter|'''pathSegTypeAsLetter''']]: Gets the type of the path segment, specified by the corresponding one-character command name.
*[[svg/properties/r1|'''r1''']]: Gets or sets the x-axis radius for an ellipse  that is associated with a [[svg/elements/path|'''path''']] element.
*[[svg/properties/r2|'''r2''']]: Gets or sets the y-axis radius for an ellipse  that is associated with a [[svg/elements/path|'''path''']] element.
*[[svg/properties/sweepFlag|'''sweepFlag''']]: Gets or sets  the value of the sweep-flag parameter.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}