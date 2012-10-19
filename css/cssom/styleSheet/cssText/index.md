{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|A style sheet in a document.}}
{{API_Object_Property
|Property_applies_to=css/cssom/styleSheet
|Read_only=No
|Example_object_name=stylesheet
|Return_value_name=cssText
|Javascript_data_type=String
|Return_value_description=The text representation of the stylesheet.
|Example_value_name=cssText
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''cssText''' property to retrieve the CSS style set on an object.
|Code=&lt;p id{{=}}"oPara" style{{=}}"color: green; font-weight: bold;"&gt;
This is the test paragraph.&lt;/p&gt;:
&lt;button onclick{{=}}"console.log(document.getElementById('oPara').style.cssText)"&gt;Get CSS attributes&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cssText.htm
}}
}}
{{Notes_Section
|Notes=This property reflects the current state of the rule and not its initial value.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Style
|URL=http://www.w3.org/TR/DOM-Level-2-Style/stylesheets.html#StyleSheets-fundamental
|Status=Recommendation
|Relevant_changes=Section 1.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
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
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}