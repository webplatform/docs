{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=Yes
|High-level issues=Copyright Issue
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the number of columns an element should be divided into.}}
{{CSS Property
|Initial value=auto
|Applies to=non-replaced block-level elements (except table elements), table cells, and inline-block elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=columnCount
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=count
|Description=An integer value that specifies the number of columns in the multi-column element. Values must be greater than 0. When [[css/properties/column-width|'''column-width''']] is specified with [[css/properties/column-count|'''column-count''']] and both have non-auto values, the integer value defines the maximum number of columns.
}}{{CSS Property Value
|Data Type=auto
|Description=The number of columns is determined by the values of other property values of the multi-column element, such as [[css/properties/column-width|'''column-width''']].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This example shows how to render text within the section.newspaper element in three columns.
|Code=#columns {
  -moz-column-count: 3; /* Firefox */
  -webkit-column-count: 3; /* Safari and Chrome */
  column-count: 3;
}
|LiveURL=http://code.webplatform.org/gist/6288917
}}{{Single Example
|Language=CSS
|Description=Using auto for column-count will allow as many columns as are necessary or able to be generated.
|Code=/* auto column-count allows n-columns of column-width */
div {
column-count: auto;
column-width: 100px;
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The actual column count may vary from the value specified due to available space.
To ensure the specified value is used, all length property values of the multi-column element must be specified.
|Import_Notes====Syntax===
<code>'''column-count: '''''count'' '''{{!}}''' auto</code>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://www.w3.org/TR/css3-multicol/
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Multi-Column, Responsive Web Design
|Manual_links=
|External_links=
|Manual_sections====Related pages===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[html/elements/table|table]]</code>

}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh772195(v=vs.85).aspx
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=4.0
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=2.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.1
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=15
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.1
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row}}
}}