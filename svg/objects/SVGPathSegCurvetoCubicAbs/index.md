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

The '''C''' object uses absolute coordinates to draw a cubic B&eacute;zier curve from the current point to (x,y) by using (x1,y1) as the control point at the beginning of the curve and (x2,y2) as the control point at the end of the curve.   You can specify multiple sets of coordinates  to draw a polyb&eacute;zier. At the end of the command, the new current point becomes the final (x,y) coordinate pair that is used in the polyb&eacute;zier.

|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204736 Scalable Vector Graphics: Paths], Section 8.5.7

===Members===

The '''SVGPathSegCurvetoCubicAbs''' object has these properties:

*[[svg/properties/pathSegType|'''pathSegType''']]: Gets the type of the path segment.
*[[svg/properties/pathSegTypeAsLetter|'''pathSegTypeAsLetter''']]: Gets the type of the path segment, specified by the corresponding one-character command name.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/x1|'''x1''']]: Gets or sets the absolute or relative x-coordinate for the first control point.
*[[svg/properties/x2|'''x2''']]: Gets or sets the absolute or relative x-coordinate for the second control point.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
*[[svg/properties/y1|'''y1''']]: Gets or sets the absolute or relative y-coordinate for the first control point.
*[[svg/properties/y2|'''y2''']]: Gets or sets the absolute or relative y-coordinate for the second control point.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}