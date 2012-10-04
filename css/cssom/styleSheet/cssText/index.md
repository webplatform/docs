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
|Description=This example uses the '''cssText''' property to retrieve the CSS style set on an object.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cssText.htm
|Code=
&lt;P ID{{=}}oPara STYLE{{=}}"color:'green'; font-weight:bold"&gt;
This is the test paragraph.&lt;/P&gt;
:
&lt;BUTTON onclick{{=}}"alert(oPara.style.cssText)"&gt;
Get CSS attributes&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property reflects the current state of the rule and not its initial value.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
*<code>[[dom/CSSFontFaceRule|CSSFontFaceRule]]</code>
*<code>[[css/cssom/CSSImportRule|CSSImportRule]]</code>
*<code>[[css/cssom/CSSMediaRule/CSSMediaRule|CSSMediaRule]]</code>
*<code>[[css/cssom/CSSNamespaceRule/CSSNamespaceRule|CSSNamespaceRule]]</code>
*<code>[[css/cssom/CSSRule/CSSRule|CSSRule]]</code>
*<code>[[css/cssom/page|page]]</code>
*<code>[[css/cssom/rule|rule]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}