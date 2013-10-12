{{Page_Title}}
{{Flags
|Checked_Out=Yes
|Editorial notes=see padding; also verify and then fix "initial value" to "browser-dependent" on padding-*
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>padding-bottom</code> CSS property of an element sets the [[css/properties/padding|padding]] space required on the bottom of an element. The padding area is the space between the content of the element and its border. Contrary to [[css/properties/margin-bottom|margin-bottom]] values, negative values of <code>padding-bottom</code> are invalid.}}
{{CSS Property
|Initial value=0
|Applies to=All elements (except table-*-group, table-row and table-column, br)
|Inherited=No
|Media=visual
|Computed value=the percentage as specified or the absolute length
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
|Code=TD { padding-bottom: 20%; }
|LiveURL=http://code.webplatform.org/gist/6948355
}}{{Single Example
|Language=CSS
|Code=TD { padding-bottom: 30px; }
|LiveURL=http://code.webplatform.org/gist/6948398
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS basic box model
|URL=http://www.w3.org/TR/css3-box/
|Status=W3C Working Draft
}}{{Related Specification
|Name=CSS 2.1, 8 Box model
|URL=http://www.w3.org/TR/CSS21/box.html#propdef-padding
|Status=W3C Recommendation
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
|Topic_clusters=CSS Layout, Box Model
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MSDN_link=
|HTML5Rocks_link=
}}