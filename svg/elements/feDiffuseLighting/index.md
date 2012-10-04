{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Notes_Section
|Notes=
===Remarks===
The resulting image is an RGBA opaque image based on the light color where alpha {{=}} 1.0.  The lighting calculation follows the standard diffuse component of the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}226233 Phong lighting model].  The resulting image depends on the light color, the light position, and the surface geometry of the input bump map.
 
 
Build date: 7/24/2012
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.13


===Members===
The '''SVGFEDiffuseLightingElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGFEDiffuseLightingElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/diffuseConstant|'''diffuseConstant''']]
|Defines the diffuse reflection constant.
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/properties/in1|'''in1''']]
|Identifies input for the given filter primitive.
|-
|[[svg/properties/kernelUnitLengthX|'''kernelUnitLengthX''']]
|<code>kernelUnitLength</code> indicates the intended distance in current filter units for ''dx'' and ''dy'' in the surface normal calculation formulas.
|-
|[[svg/properties/kernelUnitLengthY|'''kernelUnitLengthY''']]
|<code>kernelUnitLength</code> indicates the intended distance in current filter units for ''dx'' and ''dy'' in the surface normal calculation formulas.
|-
|[[svg/properties/result|'''result''']]
|Provides a reference for the output result of a filter.
|-
|[[svg/properties/width|'''width''']]
|Defines the width of an element.
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