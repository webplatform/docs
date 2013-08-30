{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the color of the rule between columns.}}
{{CSS Property
|Initial value=currentColor
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=columnRuleColor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=color
|Description=One of the color names, RGB, RGBA, HSL, or HSLA values in the [[css/color/color table|Color Table]].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Uses the column-rule-color property to set the color of the rule between columns.
|Code=/*
Makes 3 columns with 4px dashed green column-rule
*/

#columns {
  -moz-columns: 3; /* Firefox */
  -webkit-columns: 3; /* Safari and Chrome */
  columns: 3;
  
  /* Prefix free example below, use vendor prefixes where needed */
  column-rule-style: dashed;
  column-rule-color: green;
  column-rule-width: 5px;
}
|LiveURL=http://code.webplatform.org/gist/6288958
}}
}}
{{Notes_Section}}
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
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Safari
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Opera
|Version=14–Current
|Note=Requires -webkit-prefix
}}{{Compatibility Notes Row
|Browser=Firefox
|Note=Requires -moz- prefix
}}
}}
{{See_Also_Section
|Topic_clusters=Multi-Column
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}