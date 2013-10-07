{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|This property is a shorthand property for setting [[css/properties/column-width|column-width]] and/or [[css/properties/column-count|column-count]].}}
{{CSS Property
|Initial value=See individual properties.
|Applies to=Non-replaced block-level elements (except table elements), table cells, and inline-block elements.
|Inherited=No
|Media=visual
|Computed value=See individual properties.
|Animatable=No
|CSS percentages=See individual properties.
|Values={{CSS Property Value
|Data Type=column-width
|Description=Any of the values available to [[css/properties/column-width|'''column-width''']] property.
}}{{CSS Property Value
|Data Type=column-count
|Description=Any of the values available to [[css/properties/column-count|'''column-count''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Make 3 columns at auto width */
#columns {
  -moz-columns: auto 3;  /* Firefox */
  -webkit-columns: auto 3;  /* Safari and Chrome */
  columns: auto 3;
}
|LiveURL=http://code.webplatform.org/gist/6288803
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://www.w3.org/TR/css3-multicol
|Status=W3C Candidate Recommendation
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
|Sources=MDN, MSDN
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}