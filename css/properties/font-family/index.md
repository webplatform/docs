{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This property contains one or more font family names and/or generic family names. For each character that a user agent (browser) has to render, it iterates through the list of family names (first to last) until it matches a font available on the system that contains a glyph for that character.}}
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
|Description=The name of a font family, such as <code>Courier</code> or <code>Arial</code>. You can reference the common fonts available on the system, or external fonts imported using [[css/atrules/%40font-face|@font-face]]. When the family name contains more than one word, it needs to be enclosed in quotes, for example <code>'Comic Sans'</code>. 
}}{{CSS Property Value
|Data Type=generic-family
|Description=generic families are not specific fonts, but a reference to fallback fonts of a general type that can be used when specific fonts are not available. The actual fonts used for each fallback type may differ between operating systems. The following generic family keywords are defined: <code>serif</code>, <code>sans-serif</code>, <code>cursive</code>, <code>fantasy</code> and <code>monospace</code>.
}}{{CSS Property Value
|Data Type=family-name, family-name, generic-family
|Description=You can specify a comma-separated list of multiple font family names and/or generic family names, although it rarely makes sense to specify more than one generic family. This list is called a '''font-stack'''. The browser goes down the list and uses the first available font that it can find available on the system. Generic font families are used as a fallback when none of the fonts specified in the stack are available. It is always the last alternative in the list of font family names.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Define built-in fonts to use in your CSS content.
|Code=h1 { font-family: Helvetica, Arial, sans-serif; }
p { font-family: Courier, "Times New Roman", serif; }
}}{{Single Example
|Language=CSS
|Description=Adds a web font using @font-face and then assigns it to an element using font-family
|Code=/*
Defines the font and its location. font-family in this case assigns a name to the font
*/
@font-face {
  font-family: 'VeraSe';
  src: url("../_fonts/VeraSe.eot");
  src: local("☺"), 
  url("../_fonts/VeraSe.woff") format("woff"), 
  url("../_fonts/VeraSe.ttf") format("truetype"), 
  url("../_fonts/VeraSe.svg") format("svg");
  font-weight: normal;
  font-style: normal;
}

/*
We now use the name in defining the fonts for a h1 element
*/

h1 {
  font-family: VeraSe, Georgia, serif;
  margin-top: 15px;
  margin-bottom: 15px;
}
}}
}}
{{Notes_Section
|Usage=Things to note:
* If a font family name contains whitespaces, digits or punctuation characters (other than hyphens), it is recommended to place quotes around the font family name to avoid mistakes in escaping those characters
* Generic font family names are values (keywords) and cannot appear in quotation marks
* You can use font-family together with @font-face to declare and use external web fonts
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1, section 15.3
|URL=http://www.w3.org/TR/CSS21/fonts.html#font-family-prop
|Status=W3C Recommendation 07 June 2011
}}{{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/
|Status=W3C Working Draft 12 February 2013
}}{{Related Specification
|Name=CSS3 module: Web Fonts
|URL=http://www.w3.org/TR/2002/WD-css3-webfonts-20020802/
|Status=W3C Working Draft 2 August 2002
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