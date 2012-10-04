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
|Values={{CSS_Property_Value|Data Type=normal |Description=Default. Default height.}}
{{CSS_Property_Value|Data Type=height |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent sign (%). The value is a percentage of the height of the parent object.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''line-height''' attribute and the '''line-height''' property to control the height of paragraph lines.

This example uses '''p''' and '''blockquote''' as selectors in an embedded (global) style sheet to change the distance between the lines in all '''p''' and '''blockquote''' objects.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/line-height.htm
|Code=
&lt;STYLE&gt;
    P { line-height:8mm}
    BLOCKQUOTE { line-height:4mm }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the distance between lines when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/lineHeight.htm
|Code=
&lt;DIV STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.lineHeight{{=}}'6mm'"&gt;
:
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Line height is the distance between the descender of the font and the top of the internal leading of the font.
If a formatted line contains more than one object, the maximum line height applies. In this case, negative values are not allowed.
Microsoft Internet Explorer 3.0 supports the '''line-height''' attribute through the [[css/properties/font|'''font''']] attribute.
|Import_Notes=
===Syntax===
<code>'''line-height: '''normal '''{{!}}''' height '''{{!}}''' percentage</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.8


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