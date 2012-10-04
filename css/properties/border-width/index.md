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
|Values={{CSS_Property_Value|Data Type=medium |Description=Default.  }}
{{CSS_Property_Value|Data Type=thin |Description=Less than the default width.}}
{{CSS_Property_Value|Data Type=thick |Description=Greater than the default width.}}
{{CSS_Property_Value|Data Type=width |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''border-width''' attribute and the '''border-width''' property to specify the width of the border.

This example uses a call to an embedded (global) style sheet to change the width of the border to 1 centimeter when a mouse click occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-width.htm
|Code=
&lt;HEAD&gt;
&lt;STYLE&gt;
    TD { border-width:3mm }
    .changeborder1 { border-width:1cm }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt; 
&lt;TABLE BORDER&gt;
&lt;TR&gt;
    &lt;TD onclick{{=}}"this.className{{=}}'changeborder1'"
        ondblclick{{=}}"this.className{{=}}''"&gt;
        &lt;IMG src{{=}}"sphere.jpg"&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
}}
{{Single_Example
|Description=This example uses inline script to change the width of the border to 1 centimeter when a mouse click occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderWidth.htm
|Code=
&lt;TD onclick{{=}}"this.style.borderWidth{{=}}'1cm'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Up to four different widths can be specified, in the following order: top, right, bottom, left. If one width is specified, it is used for all four sides. If two widths are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three widths are specified, they are used for top, right/left, and bottom borders, respectively.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
The '''border-width''' property does not render if the [[css/properties/border-style|'''border-style''']] property is set to '''none'''.
|Import_Notes=
===Syntax===
<code>'''border-width: '''medium '''{{!}}''' thin '''{{!}}''' thick '''{{!}}''' width</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.15


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