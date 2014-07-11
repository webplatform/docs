{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, remove topic cluster flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This property transforms text for styling purposes. (It has no effect on the underlying content.)}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS percentages=no
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Text is not transformed.
}}{{CSS Property Value
|Data Type=capitalize
|Description=Transforms the first character of each word to uppercase.
}}{{CSS Property Value
|Data Type=uppercase
|Description=Transforms all the characters to uppercase.
}}{{CSS Property Value
|Data Type=lowercase
|Description=Transforms all the characters to lowercase.
}}{{CSS Property Value
|Data Type=full-width
|Description=Puts all characters in fullwidth form. If the character does not have a corresponding fullwidth form, it is left as is. This value is typically used to typeset Latin characters and digits like ideographic characters.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Examples using different values for text-transform
|Code=/*
	- text-transform property examples
	- explanations inline
*/

body {
	padding:50px;
	font-size:22px;
}

.text--uppercase {
	text-transform:uppercase; /* all uppercase characters */
}

.text--lowercase{
	text-transform: lowercase; /* all lowercase characters */
}

.text--capitalize{
	text-transform: capitalize; /* _first_ letter of each word is capitalized  */
}

.text--no-transform {
	text-transform: none; /* disables any other inherited text-transform */
}
|LiveURL=http://code.webplatform.org/gist/5651013
}}{{Single Example
|Language=CSS
|Description=Using text-transform also works on greek or german letters
|Code=/*
	- text-transform property examples
	- explanations inline
*/

body {
	padding:50px;
	font-size:22px;
}

.text--uppercase {
	text-transform:uppercase; /* works on non-latin characters as well */
}
|LiveURL=http://code.webplatform.org/gist/5651033
}}
}}
{{Notes_Section
|Notes=When using text-transform: capitalize; authors should not expect capitalize to follow language-specific titlecasing conventions (such as skipping articles in English).
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|External_links=http://www.w3.org/TR/CSS2/text.html#caps-prop

http://www.w3.org/wiki/CSS/Properties/text-transform
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}