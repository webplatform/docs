{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This property contains a comma-separated list of font family names and/or generic family names. For each character that a user agent (browser) has to render, it iterates through the list of family names (first to last) until it matches a font that contains a glyph for that character.}}
{{CSS Property
|Initial value=depends on user agent
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=fontFamily
|Values={{CSS Property Value
|Data Type=family-name
|Description=The name of a font family, such as <code>Courier</code> or <code>Arial</code>. Font family names containing whitespace should be quoted.
}}{{CSS Property Value
|Data Type=generic-family
|Description=Generic font families are used as a fallback when none of the previously specified fonts are available. It is always the last alternative in the list of font-family names. The following generic family keywords are defined: <code>serif</code>, <code>sans-serif</code>, <code>cursive</code>, <code>fantasy</code> and <code>monospace</code>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=h1 { font-family: Helvetica, Arial, sans-serif; }
p { font-family: Courier, "Times New Roman", serif; }
}}
}}
{{Notes_Section
|Usage=Things to note:
* If the font family name contains white space, it should appear in single or double quotation marks.
* Generic font family names are values (keywords) and cannot appear in quotation marks.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1, section 15.3
|URL=http://www.w3.org/TR/CSS21/fonts.html#font-family-prop
|Status=W3C Recommendation 07 June 2011
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}