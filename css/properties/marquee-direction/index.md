{{Page_Title}}
{{Flags
|Checked_Out=No
|Editorial notes=This property seems to have been deprecated. Once compatibility tables have been updated, consider a note talking about its usage.
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>marquee-direction</code> determines the initial direction in which the marquee content moves.}}
{{CSS Property
|Initial value=forward
|Applies to=non-replaced block-level elements and non-replaced ’inline-block’ elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=marqueeDirection
|CSS percentages=n/a
|Values={{CSS Property Value
|Data Type=forward
|Description=moves the content in normal reading order
}}{{CSS Property Value
|Data Type=reverse
|Description=moves the content in reverse reading order
}}
}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example
|Language=CSS
|Description=A basic example on how to use marquee-direction.
|Code=h1 {
	overflow: auto; 
	overflow-style: marquee-line;
	white-space: nowrap;
	width: 200px;
	marquee-direction: reverse;
}
|LiveURL=http://code.webplatform.org/gist/6949190
}}
}}
{{Notes_Section
|Usage=The actual direction depends the '[[css/properties/direction|direction]]' and '[[css/properties/overflow-style|overflow-style]]', as follows:

<code>overflow-style: inline; direction: ltr;marquee-direction:forward;</code><br>
animation direction: right-to-left

<code>overflow-style: inline; direction: ltr;marquee-direction:reverse;</code><br>
animation direction: left-to-right

<code>overflow-style: inline; direction: rtl;marquee-direction:forward;</code><br>
animation direction: left-to-right

<code>overflow-style: inline; direction: rtl;marquee-direction:reverse;</code><br>
animation direction: right-to-left

<code>overflow-style: block;marquee-direction:forward;</code><br>
animation direction: bottom-to-top

<code>overflow-style: block;marquee-direction:reverse;</code><br>
animation direction: top-to-bottom
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Marquee Module Level 3
|URL=http://www.w3.org/TR/css3-marquee/#marquee-direction
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