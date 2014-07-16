{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|This property specifies whether or not particularly long words will be 'broken' (separated into multiple lines) if necessary in order to fit in within its container.}}
{{CSS Property
|Initial value=normal
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=overflowWrap
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Lines can only be broken at normal break points (spaces, non-alphanumeric characters, etc.)

This is the default option.
}}{{CSS Property Value
|Data Type=break-word
|Description=Lines can be broken at any point if necessary to preserve the limits of the container element -- for example, "hamburger" can be broken into "ham" and "burger" across separate lines.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=We can compare two identical blocks of texts and see how the two possible values of '''overflow-wrap''' change the display of lines which do not fit within the container.
|Code=/* Using the CSS 'overflow-wrap' property. */
p {
	width: 5em;
	float: left;
	margin-right: 3em;
}

p:nth-child(1) {
	overflow-wrap: normal;
}

p:nth-child(2) {
	overflow-wrap: break-word;
}
|LiveURL=http://code.webplatform.org/gist/5842405
}}
}}
{{Notes_Section
|Usage=This property is only in use when [[css/properties/white-space|'''white-space''']] allows '''wrapping'''.
|Notes=[[css/properties/word-wrap|'''word-wrap''']] is a commonly used alias for '''overflow-wrap'''; specifically, '''word-wrap''' was a prior iteration of the property.  Most browsers recognize '''word-wrap''', but usage of '''overflow-wrap''' should be encouraged.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#overflow-wrap-property
|Status=Last Call Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}