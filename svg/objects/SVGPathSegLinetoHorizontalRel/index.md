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

The '''h''' object uses relative coordinates to draw a horizontal line from the current point (cpx, cpy) to (x, cpy). You can provide multiple x-coordinate values (typically, multiple coordinates do not make sense). At the end of the command, the new current point becomes (x, cpy) for the final value of x.

|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204736 Scalable Vector Graphics: Paths], Section 8.5.14

===Members===

The '''SVGPathSegLinetoHorizontalRel''' object has these properties:

*[[svg/properties/pathSegType|'''pathSegType''']]: Gets the type of the path segment.
*[[svg/properties/pathSegTypeAsLetter|'''pathSegTypeAsLetter''']]: Gets the type of the path segment, specified by the corresponding one-character command name.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}