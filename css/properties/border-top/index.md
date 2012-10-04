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
|Values={{CSS_Property_Value|Data Type=border-width |Description=Any of the range of width values available to the [[css/properties/border-top-width|'''border-top-width''']] property.}}
{{CSS_Property_Value|Data Type=border-style |Description=Any of the range of style values available to the [[css/properties/border-top-style|'''border-top-style''']] property.}}
{{CSS_Property_Value|Data Type=border-top-color |Description=Any of the range of color values available to the [[css/properties/border-top-color|'''border-top-color''']] property.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''border-top''' attribute and the '''border-top''' property to specify the composite properties.

This example uses a call to an embedded (global) style sheet to change the attributes of the top border when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-top.htm
|Code=
&lt;HEAD&gt;
&lt;STYLE&gt;
    TD 	{ border-top:0.5cm solid yellow }
    .change { border-top:0.5cm groove pink }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE&gt;
&lt;TR&gt;
    &lt;TD onmouseover{{=}}"this.className{{=}}'change'"
        onmouseout{{=}}"this.className{{=}}''"&gt;
        &lt;IMG src{{=}}"sphere.jpg"&gt;
    &lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to change the top border when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderTop.htm
|Code=
&lt;TD onmouseover{{=}}"this.style.borderTop{{=}}'0.3cm groove yellow'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''border-top''' property is a composite property that sets the '''width''', '''color''', and '''style''' values for the top border of an object.
All individual border properties not set by the composite '''border-top''' property are set to their default values. For example, the default value for '''width''' is '''medium'''.
If a '''color''' is not specified, the text color is used.
For more information about supported colors, see the Color Table.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes=
===Syntax===
<code>'''border-top: ''''''[''' ''
&lt;border-width&gt;
'' '''{{!}}{{!}}''' ''
&lt;border-style&gt;
'' '''{{!}}{{!}}''' ''
&lt;border-top-color&gt;
'' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.18


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/border|border]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
|Topic_clusters=Border
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}