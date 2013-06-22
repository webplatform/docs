{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|When non-ideographic characters (such as numbers) are presented alongside ideographic characters, many designers prefer to include spacing to separate it from the surrounding ideographs.  This property automates the creation of that space by introducing an in-line margin, the width of which corresponds to the width of existing ideographs.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=specified value (except for initial and inherit)
|Animatable=Yes
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. No effect takes place—that is, no extra space is added.
}}{{CSS Property Value
|Data Type=ideograph-alpha
|Description=Creates extra spacing between runs of ideographic and non-ideographic text, such as Latin-based, Cyrillic, Greek, Arabic, or Hebrew text.
}}{{CSS Property Value
|Data Type=ideograph-numeric
|Description=Creates extra spacing between runs of ideographic text and numeric characters.
}}{{CSS Property Value
|Data Type=ideograph-parenthesis
|Description=Creates extra spacing between a normal (non-wide) parenthesis and an ideograph.
}}{{CSS Property Value
|Data Type=ideograph-space
|Description=Extends the width of the space character when it is adjacent to ideographs.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=By setting the '''text-autospace''' property to various keywords, one can easily modify the spacing standards of combinations of ideographic and non-ideographic characters.
|Code=/**
 * Using the CSS `text-autospace` property.
 */

tr:nth-child(3) {
	text-autospace: ideograph-numeric;
}

tr:nth-child(4) {
	text-autospace: ideograph-alpha;
}

tr:nth-child(5) {
	text-autospace: ideograph-parenthesis;
}
|LiveURL=http://code.webplatform.org/gist/5842252
}}
}}
{{Notes_Section
|Usage=This property acts in addition to other properties such as [[css/properties/word-spacing]] and [[css/properties/letter-spacing]], meaning that you can use both properties and their effects will be compounded.

This property is not currently supported by any major browser.
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-text-autospace''' attribute is an extension to CSS, and can be used as a synonym for '''text-autospace''' in IE8 Standards mode.
An ideograph is a character in an Asian writing system that represents a concept or an idea, but not a particular word or pronunciation.
|Import_Notes====Syntax===
<code>'''-ms-text-autospace: '''none '''{{!}}''' ideograph-alpha '''{{!}}''' ideograph-numeric '''{{!}}''' ideograph-parenthesis '''{{!}}''' ideograph-space</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 9.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}