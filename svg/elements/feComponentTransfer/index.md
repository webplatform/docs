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
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
This filter primitive performs component-wise remapping of data as follows for every pixel:
It allows operations like brightness adjustment, contrast adjustment, color balance, or thresholding.
The <code>feFuncR</code>, <code>feFuncG</code>, <code>feFuncB</code>, and<code>feFuncA</code> elements can be children of the <code>feComponentTransfer</code> element. For more information, see [[svg/elements/feFuncR|'''SVGFEFuncRElement''']].
The calculations are performed on non-premultiplied color values. If the input graphics consist of premultiplied color values, those values are automatically converted into non-premultiplied color values for this operation. (Note that the undoing and redoing of the premultiplication can be avoided if [[svg/elements/feFuncA|'''feFuncA''']] is the identity transform and all alpha values on the source graphic are set to 1.)
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.5


===Members===
The '''SVGFEComponentTransferElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGFEComponentTransferElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/properties/in1|'''in1''']]
|Identifies input for the given filter primitive.
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
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/feFuncR|SVGFEFuncRElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}