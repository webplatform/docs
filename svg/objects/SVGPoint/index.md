{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
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
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
An '''SVGPoint''' object is an (x, y) coordinate pair. When you use an '''SVGPoint''' object  in matrix operations,  the object is treated as a vector of the following form.

 
 
Build date: 7/24/2012
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204735 Scalable Vector Graphics: Coordinate Systems, Transformations and Units], Section 7.14.1


===Members===
The '''SVGPoint''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''SVGPoint''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/matrixTransform|'''matrixTransform''']]
|Applies the given 2×3 matrix transformation on this '''SVGPoint''' object and returns a new, 
transformed '''SVGPoint''' object.
|}
 

====Properties====
The '''SVGPoint''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/x|'''x''']]
|Gets or sets the x-coordinate value.
|-
|[[svg/properties/y|'''y''']]
|Gets or sets the y-coordinate value.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}