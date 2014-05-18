{{Page_Title|::first-line}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents the first line of an element. Note that the content of the first line varies depending on the available width and the styling of text (size, spacing).}}
{{CSS_Selector
|Content====Syntax===
{{Single Example
|Language=CSS
|Code=::first-line {}
}}
===Usage===
The ::first-line pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding display property to block.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example puts the first line of any paragraph in bold text
|Code=p::first-line {
	font-weight: bold;
}
|LiveURL=https://code.webplatform.org/gist/fe1382a764e07a9c7917
}}
}}
{{Notes_Section
|Notes====Remarks===
Only the following properties apply to the ::first-letter pseudo-element:
[[css/properties/background|'''background''']], [[css/properties/clear|'''clear''']], [[css/properties/color|'''color''']], [[css/properties/font|'''font''']], [[css/properties/font-family|'''font-family''']], [[css/properties/font-size|'''font-size''']], [[css/properties/font-style|'''font-style''']], [[css/fonts/font-variant|'''font-variant''']], [[css/properties/font-weight|'''font-weight''']], [[css/properties/line-height|'''line-height''']], [[css/properties/text-decoration|'''text-decoration''']], 
[[css/properties/text-transform|'''text-transform''']], [[css/properties/vertical-align|'''vertical-align''']], and [[css/text/word-spacing/word-spacing|'''word-spacing''']]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C CSS 2.1 Selectors
|URL=http://www.w3.org/TR/CSS2/selector.html#first-line-pseudo
|Status=W3C Recommendation
}}{{Related Specification
|Name=W3C CSS Selectors Level 3
|URL=http://www.w3.org/TR/css3-selectors/#first-line
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=< 9
|Note=Only the one-colon form of this pseudo-element is recognized—that is, ''':first-line'''. Beginning with Internet Explorer 9, the '''::first-line''' pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form.
}}
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Elements, Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|HTML5Rocks_link=
}}