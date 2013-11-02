{{Page_Title}}
{{Flags
|Checked_Out=No
|Editorial notes=This property seems to have been deprecated. Once compatibility tables have been updated. Consider a note talking about its usage.
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>marquee-speed</code> determines how fast the marquee content scrolls.}}
{{CSS Property
|Initial value=normal
|Applies to=non-replaced block-level elements and non-replaced ’inline-block’ elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=marqueeSpeed
|CSS percentages=n/a
|Values={{CSS Property Value
|Data Type=slow
|Description=slower than normal
}}{{CSS Property Value
|Data Type=normal
|Description=faster than slow, slower than fast
}}{{CSS Property Value
|Data Type=fast
|Description=faster than normal
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=A basic example on how to use marquee-speed.
|Code=h1 {
	overflow: auto; 
	overflow-style: marquee-line;
	white-space: nowrap;
	width: 200px;
	marquee-speed: fast;
}
|LiveURL=http://code.webplatform.org/gist/6948165
}}
}}
{{Notes_Section
|Notes=The actual speed depends on the UA and the type of content.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Marquee Module Level 3
|URL=http://www.w3.org/TR/css3-marquee/#marquee-speed
|Status=Candidate Recommendation
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