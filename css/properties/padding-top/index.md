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
|Initial value=0
|Values={{CSS_Property_Value|Data Type=length |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''padding-top''' attribute and the '''padding-top''' property to change the padding of the object.

This example uses '''td''' as a selector in an embedded style sheet to set the top padding for all table cells to 1 centimeter.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/padding-top.htm
|Code=
&lt;STYLE&gt;
    TD { padding-top:1cm }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the cell's top padding to 1 centimeter when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/paddingTop.htm
|Code=
&lt;TD onmouseover{{=}}"this.style.paddingTop{{=}}'1cm'"
    onmouseout{{=}}"this.style.paddingTop{{=}}''"&gt;
    &lt;IMG src{{=}}"sphere.jpg"&gt;
&lt;/TD&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
Negative values are not allowed.
|Import_Notes=
===Syntax===
<code>'''padding-top: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Box Model
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}