{{Page_Title|text-emphasis}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The text-emphasis property will apply special emphasis marks to the elements text. Slightly similar to the text-decoration property only that this property can have affect on the line-height. It also is noted that this is shorthand for text-emphasis-style and for text-emphasis-color.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=none
|Animatable=No
|CSS object model property=textEmphasis
|CSS percentages=Not available
|Values={{CSS Property Value
|Data Type=none
|Description=There are no emphasis marks
}}{{CSS Property Value
|Data Type=filled
|Description=It is filled with a solid color
}}{{CSS Property Value
|Data Type=open
|Description=The shape has an empty space
}}{{CSS Property Value
|Data Type=dot
|Description=Displays small circles as marks
}}{{CSS Property Value
|Data Type=circle
|Description=Displays large circles as marks
}}{{CSS Property Value
|Data Type=double-circle
|Description=Displays double circles as marks
}}{{CSS Property Value
|Data Type=triangle
|Description=Displays triangles as marks
}}{{CSS Property Value
|Data Type=sesame
|Description=Displays sesames as marks
}}{{CSS Property Value
|Data Type=<string>
|Description=Display the given string as marks. Authors should not specify more than one character in <string>. The UA may truncate or ignore strings consisting of more than one grapheme cluster.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=p {
  /*text-emphasis: shape color;*/
  text-emphasis: triangle #f70;
}
|LiveURL=http://code.webplatform.org/gist/6133067
}}{{Single Example
|Language=CSS
|Code=p {
  /*text-emphasis: "string";*/
  text-emphasis: "*";
}
}}{{Single Example
|Language=CSS
|Code=p {
  /*text-emphasis: "string" color;*/
  text-emphasis: "^" #ccc;
}
}}
}}
{{Notes_Section
|Notes=Don't apply on special word separators like spaces.

Size of the marks will always scale to 50% of the container's actual font size.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Decoration Module Level 3
|URL=http://dev.w3.org/csswg/css-text-decor-3/#emphasis-marks
|Status=Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Yes
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Yes
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
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