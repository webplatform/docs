{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|On inline elements, the line-height CSS property specifies the height that is used in the calculation of the line box height.
On block level elements, line-height specifies the minimal height of line boxes within the element.
}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Default height. Depends on the user agent.
}}{{CSS Property Value
|Data Type=<number>
|Description=The used value of the property is this number multiplied by the element's font size. Negative values are illegal.
}}{{CSS Property Value
|Data Type=<length>
|Description=The specified length is used in the calculation of the line box height. Negative values are illegal.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=The computed value of the property is this percentage multiplied by the element's computed font size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''line-height''' attribute and the '''line-height''' property to control the height of paragraph lines.

This example uses '''p''' and '''blockquote''' as selectors in an embedded (global) style sheet to change the distance between the lines in all '''p''' and '''blockquote''' objects.
|Code=&lt;STYLE&gt;
    P { line-height:8mm}
    BLOCKQUOTE { line-height:4mm }
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/line-height.htm
}}{{Single Example
|Description=This example uses inline scripting to set the distance between lines when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;DIV STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.lineHeight{{=}}'6mm'"&gt;
:
&lt;/DIV&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/lineHeight.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Line height is the distance between the descender of the font and the top of the internal leading of the font.
If a formatted line contains more than one object, the maximum line height applies. In this case, negative values are not allowed.
Microsoft Internet Explorer 3.0 supports the '''line-height''' attribute through the [[css/properties/font|'''font''']] attribute.
|Import_Notes====Syntax===
<code>'''line-height: '''normal '''{{!}}''' height '''{{!}}''' percentage</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.8
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
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/line-height
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}