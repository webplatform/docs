{{Page_Title}}
{{Flags
|Content=Examples Best Practices
|Checked_Out=Yes
|Editorial notes=see padding; also verify and then fix "initial value" to "browser-dependent" on padding-*
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>padding-bottom</code> is an optional CSS property of an element that sets the [[css/properties/padding|padding]] space required below an element.  The padding area is the space between an element and its border. Negative values are not allowed but decimal values are permitted. The element size is treated as fixed, and the content of the element shifts toward the center as padding is increased.  Negative values are not permitted.}}
{{CSS Property
|Initial value=0
|Applies to=All elements (except table-*-group, table-row and table-column, br)
|Inherited=No
|Media=visual
|Computed value=the percentage as specified or the element's absolute length
|Animatable=Yes
|CSS percentages=refer to [[css/properties/width|width]] of closest block-level ancestor
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a positive fixed distance. See [[css/data_types/length|length]] for details.
}}{{CSS Property Value
|Data Type=percentage
|Description=Calculated using the dimensions of the containing block or element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the <code>padding-bottom</code> property to change the [[css/properties/padding|padding]] of the elements.
|Code=h1 { padding-bottom: 5%; }

}}{{Single Example
|Language=CSS
|Code=p { padding-bottom: 10px; }
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Box Model
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MSDN_link=
|HTML5Rocks_link=
}}