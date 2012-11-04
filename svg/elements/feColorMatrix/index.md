{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes=This is a mis-spelling of feColorMatrix (there is no feColorMix) - and looks like  a garbled import
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This filter applies the following matrix transformation:
<code>{{!}} R' {{!}}     {{!}} a00 a01 a02 a03 a04 {{!}}   {{!}} R {{!}}
{{!}} G' {{!}}     {{!}} a10 a11 a12 a13 a14 {{!}}   {{!}} G {{!}}
{{!}} B' {{!}}  {{=}}  {{!}} a20 a21 a22 a23 a24 {{!}} * {{!}} B {{!}}
{{!}} A' {{!}}     {{!}} a30 a31 a32 a33 a34 {{!}}   {{!}} A {{!}}
{{!}} 1  {{!}}     {{!}}  0   0   0   0   1  {{!}}   {{!}} 1 {{!}}
</code>
This matrix is applied on the RGBA color and alpha values of every pixel on the input graphics to produce a result with a new set of RGBA color and alpha values.
The calculations are performed on non-premultiplied color values. If the input graphics consist of premultiplied color values, those values are automatically converted into non-premultiplied color values for this operation.
The <code> type</code> attributed is used to indicate the type of matrix operation. The keyword <code>matrix</code> indicates that a full 5x4 matrix of values will be provided. The other keywords (see [[svg/properties/values|'''values''']]) represent convenience shortcuts to allow commonly used color operations to be performed without specifying a complete matrix. If the attribute <code>type</code> is not specified, the effect is as if a value of <code>matrix</code> were specified.
 
 
Build date: 7/24/2012
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.4


===Members===
The '''SVGFEColorMatrixElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGFEColorMatrixElement''' object has these properties.
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
|[[svg/properties/type (SVGFEColorMatrixElement)|'''type''']]
|Indicates the type of matrix operation.
|-
|[[svg/properties/values|'''values''']]
|Numeric values for the '''feColorMatrix''' transformation matrix.
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