{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=width
|Description=Any of the range of width values available to the [[css/properties/border-left-width|'''border-left-width''']] property.
}}{{CSS Property Value
|Data Type=style
|Description=Any of the range of style values available to the [[css/properties/border-left-style|'''border-left-style''']] property.
}}{{CSS Property Value
|Data Type=color
|Description=Any of the range of color values available to the [[css/properties/border-left-color|'''border-left-color''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-right''' property and the '''border-right''' attribute to specify the composite properties.

This example uses a call to an embedded (global) style sheet to change the attributes of the right border when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
    TD { border-right-style:solid; border-width:0.3cm }
    .change { border-right-style:groove }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt; 
&lt;TABLE&gt; 
&lt;TR&gt; 
    &lt;TD onmouseover{{=}}"this.className{{=}}'change'" 
        onmouseout{{=}}"this.className{{=}}''"&gt;
        &lt;IMG src{{=}}"sphere.jpg"&gt;&lt;/TD&gt; 
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-right.htm
}}{{Single Example
|Description=This example uses inline scripting to change the attributes of the right border when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;TD onmouseover{{=}}"this.style.borderRight{{=}}'0.3cm groove yellow'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderRight.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-right''' property is a composite property that sets the '''width''', '''style''', and '''color''' values for the right border of an object.
All individual border properties not set by the composite '''border-right''' property are set to their default values. For example, the default value for '''width''' is '''medium'''.
If a '''color''' is not specified, the text color is used.
For more information about supported colors, see the Color Table.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes====Syntax===
<code>'''border-right: ''''''[''' width '''{{!}}{{!}}''' style '''{{!}}{{!}}''' ''
&lt;color&gt;
'' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.19
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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