{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the width of the rule between columns.}}
{{CSS Property
|Initial value=medium
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Computed value=absolute length; ‘0’ if the column rule style is ‘none’ or ‘hidden’
|Animatable=Yes
|CSS object model property=columnRuleWidth
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=medium
|Description=Default. A medium width border.
}}{{CSS Property Value
|Data Type=thin
|Description=Width less than the default.
}}{{CSS Property Value
|Data Type=thick
|Description=Width greater than the default.
}}{{CSS Property Value
|Data Type=width
|Description=Width consisting of a floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>)
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Makes 3 columns with 4px dashed green column-rule.
|Code=#columns {
  -moz-column-rule: 3; /* Firefox */
  -webkit-column-count: 3; /* Safari and Chrome */
  column-count: 3;
  -moz-column-rule: dashed green; /* Firefox */
  -webkit-column-rule: dashed green; /* Safari and Chrome */
  column-rule: dashed green;
  -moz-column-rule-width: 4px; /* Firefox */
  -webkit-column-rule-width: 4px; /* Safari and Chrome */
  column-rule-width: 4px;
}
|LiveURL=http://code.webplatform.org/gist/6311393
}}
}}
{{Notes_Section
|Usage=* Negative length values are not allowed.
|Notes=The exact thickness of the column rule when using the <code>medium</code>, <code>thin</code>, or <code>thick</code> value is user agent dependent, and is not defined in the specification.
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
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Safari
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Opera
|Note=Requires -webkit- prefix
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