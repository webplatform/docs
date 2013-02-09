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
|Description=The name of a font family, such as <code>Courier</code> or <code>Arial</code>.
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
* If a font family name contains whitespaces, digits or punctuation characters (other than hyphens), it is recommended to place quotes around the font family name to avoid mistakes in escaping those characters.
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
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=IE
|Version=8
|Note=IE8 requires a !DOCTYPE
}}{{Compatibility Notes Row
|Browser=IE
|Version=7
|Note=The value "inherit" is not supported in IE7 and earlier.
}}
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts
|External_links=* [http://mathiasbynens.be/notes/unquoted-font-family Unquoted font family names in CSS]
* [http://dev.w3.org/csswg/css3-fonts/#font-family-prop Basic Font Properties]
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