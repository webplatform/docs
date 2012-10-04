{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=length |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent sign (%). The value is a percentage of the width or height of the object.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''background-position''' attribute and the '''background-position''' property to specify the position of a background image.

This example uses a call to an embedded (global) style sheet to move the sphere.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-position.htm
|Code=
&lt;STYLE&gt;
    .style1 { background-position:top center }
    .style2 { background-position:bottom right }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"oSpan.className{{=}}'style1'"&gt;
&lt;SPAN STYLE{{=}}"font-size:14; width:250;" ID{{=}}"oSpan"
    onmouseover{{=}}"this.className{{=}}'style2'" onmouseout{{=}}"this.className{{=}}'style1'"&gt;
. . . &lt;/SPAN&gt;
}}
{{Single_Example
|Description=This example uses an inline style to move the sphere.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundPosition.htm
|Code=
&lt;SPAN onmouseover{{=}}"this.style.backgroundPosition{{=}}'bottom right'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
If only one value is set, that value applies to the horizontal coordinate, and the vertical is set to <code>50%</code>. If both values are set, the first value applies to the horizontal coordinate and the second value applies to the vertical.
Setting the values to <code>0% 0%</code> (initial value) positions the [[css/properties/background-image|'''background-image''']] to the upper left corner of the element's content block, which includes the padding.
Setting the background position using pixels positions the upper-left of the image at the specified x and y coordinates within the parent element. As the coordinates increase, the image moves to the right and down the visible area. By contrast, setting the background position with percentages uses a corresponding point on the image. At a position of <code>50% 50%</code> the image is effectively centered within the visible area.
This property can be set with the other background properties using the [[css/cssom/properties/background|'''background''']] composite property.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], '''background-position''', [[css/properties/background-repeat|'''background-repeat''']], and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes=
===Syntax===
<code>'''background-position: ''''''[''' '''[''' percentage '''{{!}}''' length '''{{!}}''' left '''{{!}}''' center '''{{!}}''' right ''']''' '''[''' percentage '''{{!}}''' length '''{{!}}''' top '''{{!}}''' center '''{{!}}''' bottom ''']''''''?''' ''']''' '''{{!}}''' '''[''' '''[''' left '''{{!}}''' center '''{{!}}''' right ''']''' '''{{!}}{{!}}''' '''[''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Background
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}