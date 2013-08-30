{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>column-span</code> CSS property makes it possible for an element to span across all columns when its value is set to all. An element that spans more than one column is called a spanning element.}}
{{CSS Property
|Initial value=none
|Applies to=block-level elements, except floating and absolutely positioned elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=columnSpan
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. The content block does not span multiple columns.
}}{{CSS Property Value
|Data Type=all
|Description=The content block spans all columns on a page. All content that is declared before the content block is shown before the content block.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Makes 4 columns and creates a span that crosses through columns
|Code=/*
Makes 4 columns and creates a span that crosses through columns
*/

#column {
  /* Prefix free example below, use vendor prefixes where needed */
  column-count: 4;
  column-gap: 2em;          
  padding: 5px;
}

.span-content {
  column-span: all;
}
|LiveURL=http://code.webplatform.org/gist/5306158
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.1+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.1+
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Safari
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Opera
|Version=14–Current
|Note=Requires -webkit- prefix
}}
}}
{{See_Also_Section
|Topic_clusters=Multi-Column
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/column-span
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}