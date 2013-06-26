{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This property specifies how far an absolutely positioned box's top margin edge is offset below the top edge of the box's containing block. For relatively positioned boxes, the offset is with respect to the top edges of the box itself (i.e., the box is given a position in the normal flow, then offset from that position according to these properties).}}
{{CSS Property
|Initial value=auto
|Applies to=Positioned elements
|Inherited=No
|Media=visual
|Computed value=for 'position:relative', see Relative Positioning. For 'position:static', 'auto'. Otherwise: if specified as a length, the corresponding absolute length; if specified as a percentage, the specified value; otherwise, 'auto'.
|Animatable=No
|CSS percentages=refer to height of containing block
|Values={{CSS Property Value
|Data Type=auto
|Description=For non-replaced elements, the effect of this value depends on which of related properties have the value 'auto' as well. See the sections on the width and height of absolutely positioned, non-replaced elements for details. For replaced elements, the effect of this value depends only on the intrinsic dimensions of the replaced content. See the sections on the width and height of absolutely positioned, replaced elements for details
}}{{CSS Property Value
|Data Type=length
|Description=The offset is a fixed distance from the reference edge. Negative values are allowed. For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=The offset is a percentage of the containing block's width (for 'left' or 'right') or height (for 'top' and 'bottom'). Negative values are allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''top''' attribute and the '''top''' property to change the position of the object.

This example uses an inline style to set the position of a '''div''' object.
|Code=&lt;DIV STYLE{{=}}"position:absolute;top:100px"&gt;
. . . &lt;/DIV&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/top_h.htm
}}{{Single Example
|Description=This example uses inline script to change the position of the image set by an inline style. The change occurs during [[dom/events/mouseover|'''onmouseover''']] and [[dom/events/mouseout|'''onmouseout''']] events.
|Code=&lt;IMG SRC{{=}}"cone.jpg" STYLE{{=}}"position:absolute; 
    top:80px;" onmouseover{{=}}"this.style.top{{=}}'100px''"    
    onmouseout{{=}}"this.style.top{{=}}'80px'" &gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/top_s.htm
}}
}}
{{Notes_Section
|Notes=For absolutely positioned elements whose containing block is based on a block-level element, this property is an offset from the padding edge of that element.

===Remarks===
The '''top''' attribute should be used only when the [[css/properties/position|'''position''']] attribute is set; otherwise, the value of the '''top''' attribute is ignored.
Because the value of the '''top''' property is a string, you cannot use the property in script to calculate the position of the object in the document; instead, use the [[css/cssom/properties/pixelTop|'''pixelTop''']] or the [[css/cssom/properties/posTop|'''posTop''']] property.
For more information about how to access the dimension and location of objects on the document through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes====Syntax===
<code>'''top: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
'' '''{{!}}''' auto</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 9.3.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification
|URL=http://www.w3.org/TR/2007/CR-CSS21-20070719/visuren.html#position-props
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/cssom/properties/pixelTop|pixelTop]]</code>
*<code>[[css/cssom/properties/posTop|posTop]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}