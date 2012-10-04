{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''font-variant''' attribute and the '''font-variant''' property to change the font to small capitals.

This example uses P as a selector in an embedded (global) style sheet to set the font style to '''small-caps''' in all paragraphs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font-variant.htm
|Code=
&lt;P STYLE{{=}}"font-variant:small-caps"&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the font style to '''small-caps''' when an [[dom/events/mousedown|'''onmousedown''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontVariant.htm
|Code=
&lt;DIV onmousedown{{=}}"this.style.fontVariant{{=}}'small-caps'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Microsoft Internet Explorer 4.0 renders '''small-caps''' as uppercase letters in a smaller size.
|Import_Notes=
===Syntax===
<code>'''font-variant: '''normal '''{{!}}''' small-caps</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
|Topic_clusters=Fonts
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}