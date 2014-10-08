{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>padding-top</code> CSS property of an element sets the [[css/properties/padding|padding]] space required on the top of an element. The padding area is the space between the content of the element and its border. Contrary to [[css/properties/margin-top|margin-top]] values, negative values of <code>padding-top</code> are invalid.}}
{{CSS Property
|Initial value=0
|Applies to=all elements (except table-*-group, table-row and table-column, br)
|Inherited=No
|Media=visual
|Computed value=the percentage as specified or the absolute length
|Animatable=Yes
|CSS object model property=
|CSS percentages=refer to [[css/properties/width|width]] of closest block-level ancestor
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a positive fixed distance. See [[css/data_types/length|length]] for details.
}}{{CSS Property Value
|Data Type=percentage
|Description=A percentage with respect to the height of the containing block.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the '''padding-top''' property to change the padding of the elements.
|Code=TD { padding-top: 20%; }
|LiveURL=http://code.webplatform.org/gist/6948436
}}{{Single Example
|Language=CSS
|Description=
|Code=TD { padding-top: 30px; }
|LiveURL=http://code.webplatform.org/gist/6948429
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes====Syntax===
<code>'''padding-top: '''''
&lt;length&gt;
'' {{!}} ''
&lt;percentage&gt;
''</code>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS basic box model
|URL=http://www.w3.org/TR/css3-box/
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=CSS 2.1, 8 Box model
|URL=http://www.w3.org/TR/CSS21/box.html#propdef-padding
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}