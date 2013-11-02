{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies how to fill columns (balanced or sequential).}}
{{CSS Property
|Initial value=balance
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=balance
|Description=Columns are filled sequentially such that the column heights are balanced as equally as possible, depending on other column property values.
}}{{CSS Property Value
|Data Type=auto
|Description=Columns are filled sequentially such that the columns may differ in length, depending on other column property values.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
Make as many 15em columns as possible 
but restrict the heights of the columns to 400px 
with column-fill: balance;
*/

#columns {  
  /* Prefix free example below, use vendor prefixes where needed */
  column-width: 15em;
  column-fill: balance;
  height: 400px;
}
|LiveURL=http://code.webplatform.org/gist/6393571
}}
}}
{{Notes_Section
|Notes=In continuous media, this property will only be consulted if the length of columns has been constrained. Otherwise, columns will automatically be balanced.

In continous media, this property does not have any effect in overflow columns; in paged media, this property will only have effect on the last page the multicol element appears on.

Column balancing is also dependent on the values of [[css/properties/orphans|orphans]] and [[css/properties/widows|widows]], if set.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://www.w3.org/TR/css3-multicol/
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
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh772197(v=vs.85).aspx
|HTML5Rocks_link=
}}