{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Used to alter the default CSS box model used to calculate widths and heights of elements.}}
{{CSS Property
|Applies to=all elements that accept width or height
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=content-box
|Description=The width and height properties are measured including only the content, but not the border, margin, or padding. This is the behaviour of width and height as specified by CSS2.1
}}{{CSS Property Value
|Data Type=padding-box
|Description=The width and height include the padding size, but they do not include the border or margin.
}}{{CSS Property Value
|Data Type=border-box
|Description=The width and height include the padding and border, but not the margin. 
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* support Firefox, WebKit, Opera and IE8+ */
 
div{
  -moz-box-sizing: border-box;
       box-sizing: border-box;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C
|URL=http://dev.w3.org/csswg/css3-ui/#box-sizing
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=9
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.1
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Visual Effects
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/box-sizing
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}