{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Border-collapse can be used for collapsing the borders between table cells.}}
{{CSS Property
|Initial value=separate
|Applies to=Table and inline-table elements
|Inherited=Yes
|Media=visual
|Animatable=No
|CSS object model property=borderCollapse
|Values={{CSS Property Value
|Data Type=separate
|Description=Default. Borders are detached (standard HTML). Each table cell has an individual border, with optional space between the borders.
}}{{CSS Property Value
|Data Type=collapse
|Description=Adjacent borders and the space between them are collapsed into a single border.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Example of a basic border-collapse.
|Code=table {
	border-collapse: separate; /* default */
}
table.collapse {
	border-collapse: collapse;
}
|LiveURL=http://code.webplatform.org/gist/6948189
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS2.1, section 17.6 Borders
|URL=http://www.w3.org/TR/CSS2/tables.html#propdef-border-collapse
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Tables
|Manual_links=*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}