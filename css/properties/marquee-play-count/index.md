{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
This property seems to have been deprecated. Once compatibility tables have been updated, consider a note talking about its usage.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|This property specifies how many times the marquee content moves}}
{{CSS Property
|Initial value=1
|Applies to=non-replaced block-level elements and non-replaced ’inline-block’ elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=marqueePlayCount
|CSS percentages=n/a
|Values={{CSS Property Value
|Data Type=<non-negative-integer>
|Description=Any value of 0 and higher. If the value is greater than 16, the UA may stop after 16 loops.
}}{{CSS Property Value
|Data Type=infinite
|Description=An infinite loop. The UA may stop after 16 loops.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=h1 {
	overflow: auto; 
	overflow-style: marquee-line;
	white-space: nowrap;
	width: 200px;
	marquee-play-count: 2;
}
|LiveURL=http://code.webplatform.org/gist/6948452
}}
}}
{{Notes_Section
|Usage=If <code>marquee-play-count</code> changes because of a state change (e.g. on hover), the loop counter will reset of the computed value differs:

For example:
<code>
  h1 { marquee-play-count: 2; }
  h1:hover { marquee-play-count: 4;}
</code>

Now, the <code>h1</code> loops 2 times, until you hover over it. Then the loop counter will reset and it loops for 4 times. If you than leave the element, it resets again and it will loop 2 times.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Marquee Module Level 3
|URL=http://www.w3.org/TR/css3-marquee/#the-marquee-play-count
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