{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The text-overflow-ellipsis CSS property controls how the hint on overflowed content that is not displayed is signaled to the users. The presence of the hint is controlled with CSS property [[css/properties/text-overflow-mode|text-overflow-mode]]. Shorthand property is [[css/properties/text-overflow|text-overflow]].}}
{{CSS Property
|Initial value=U+2026
|Applies to=block-level and inline-block elements
|Inherited=No
|Media=visual
|Computed value=specified value (except for initial and inherit)
|Animatable=No
|CSS object model property=text-overflow-ellipsis
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=string
|Description=The value is defined either as a string like the default UTF-8 character 'U+2026' or a URI and represents the ellipsis of text-overflow-mode property. If the value is defined as a URI it displays the image behind the URL. You can also set both values which then means they determine the overflow visual hint at the end and the hint after the element box. The latter visual hint is only displayed if there is clipped content because of the dimension limitation on the element block.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- example showing text-overflow-ellipsis property --&gt;

&lt;div class=&quot;overflowed overflowed-ellipsis&quot;&gt;
	&lt;p&gt;This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.&lt;/p&gt;
&lt;/div&gt;
&lt;div class=&quot;overflowed overflowed-ellipsis-word&quot;&gt;
	&lt;p&gt;This is an example text showing nothing interesting but the truncated content via text-overflow shorthand property.&lt;/p&gt;
&lt;/div&gt;
|LiveURL=http://dabblet.com/gist/4744982
}}{{Single Example
|Language=CSS
|Code=.overflowed > p{
	width: 10em;
	height: 5em;
	white-space: nowrap; 
	overflow: hidden;
}

.overflowed-ellipsis > p {
	text-overflow-mode: ellipsis;
	text-overflow-ellipsis: '[more]';
}

.overflowed-ellipsis-word > p {
	text-overflow-mode: ellipsis-word;
	text-overflow-ellipsis: '[more]';
}
|LiveURL=http://dabblet.com/gist/4744982
}}
}}
{{Notes_Section
|Usage=Currently it is not widely supported in any major browsers.
|Notes=Because the initial value (U+2026) of the overflow visual hint after the element box may not be easily rendered in some situations, the user agent may replace it by a sequence of 3 FULL STOP characters (U+002E).
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=css/properties/text-overflow
}}
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=text-overflow-ellipsis
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Attributes, Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}