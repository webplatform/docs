{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets all the top border properties in one declaration.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=border-width
|Description=Any of the range of width values available to the [[css/properties/border-top-width|'''border-top-width''']] property.
}}{{CSS Property Value
|Data Type=border-style
|Description=Any of the range of style values available to the [[css/properties/border-top-style|'''border-top-style''']] property.
}}{{CSS Property Value
|Data Type=border-top-color
|Description=Any of the range of color values available to the [[css/properties/border-top-color|'''border-top-color''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-top''' attribute and the '''border-top''' property to specify the composite properties.

This example uses a call to an embedded (global) style sheet to change the attributes of the top border when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;HEAD&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-top.htm
}}{{Single Example
|Description=This example uses inline scripting to change the top border when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;TD onmouseover{{=}}"this.style.borderTop{{=}}'0.3cm groove yellow'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderTop.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-top''' property is a composite property that sets the '''width''', '''color''', and '''style''' values for the top border of an object.
All individual border properties not set by the composite '''border-top''' property are set to their default values. For example, the default value for '''width''' is '''medium'''.
If a '''color''' is not specified, the text color is used.
For more information about supported colors, see the Color Table.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes====Syntax===
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
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/border|border]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}