{{Page_Title}}
{{Flags
|Content=Broken Links, Examples Best Practices
|Checked_Out=Yes
|Editorial notes=see padding-bottom
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>padding-left</code> CSS property of an element sets the [[css/properties/padding|padding]] space required on the left side of an element. The padding area is the space between the content of the element and its border. Negative values are not allowed.}}
{{CSS Property
|Initial value=0
|Applies to=All elements (except table-*-group, table-row and table-column)
|Inherited=No
|Media=visual
|Computed value=the percentage as specified or the absolute length
|Animatable=Yes
|CSS percentages=refer to [[css/properties/width|width]] of closest block-level ancestor
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a positive fixed width. See [[css/properties/length|length]] for details.
}}{{CSS Property Value
|Data Type=percentage
|Description=A percentage with respect to the width of the containing block.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the <code>padding-left</code> property to change the [[css/properties/padding|padding]] of the elements.
|Code=h1 { padding-left: 5%; }
p { padding-left: 10px; }
}}{{Single Example
|Language=HTML
|Code=&lt;h1&gt;Hey there&lt;/h1&gt;
&lt;p&gt;I think you are awesome!&lt;/p&gt;
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
<code>padding-left: &lt;length&gt; {{!}} &lt;percentage&gt; {{!}} inherit;</code>
}}
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