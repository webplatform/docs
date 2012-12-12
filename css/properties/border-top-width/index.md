{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the width of an element's top border.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=medium
|Description=Default.  
}}{{CSS Property Value
|Data Type=thin
|Description=Less than the default width.
}}{{CSS Property Value
|Data Type=thick
|Description=Greater than the default width.
}}{{CSS Property Value
|Data Type=width
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-top-width''' attribute and the '''border-top-width''' property to specify the width of the top border.

This example uses a call to an embedded (global) style sheet to change the width of the top border to 1 centimeter when a mouse click occurs.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
    TD { border-top-width:3mm }
    .changeborder1 { border-top-width:1cm }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt;
    &lt;TD onclick{{=}}"this.className{{=}}'changeborder1'"
        ondblclick{{=}}"this.className{{=}}''"&gt;
        &lt;IMG src{{=}}"sphere.jpg"&gt;
    &lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-top-width.htm
}}{{Single Example
|Description=This example uses inline script to change the width of the top border to 1 centimeter when a mouse click occurs.
|Code=&lt;TD onclick{{=}}"this.style.borderTopWidth{{=}}'1cm'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderTopWidth.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes====Syntax===
<code>'''border-top-width: '''medium '''{{!}}''' thin '''{{!}}''' thick '''{{!}}''' width</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.11
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