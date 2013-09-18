{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|When a grid container does not specify an automatic-placement strategy (through [[css/properties/grid-auto-flow|grid-auto-flow]]), any grid items that must be automatically placed are all placed at the position specified by this property. That is, the two <grid-line> values are treated as though they were specified by [[css/properties/grid-column-start|grid-column-start]] and [[css/properties/grid-column-end|grid-column-end]].}}
{{CSS Property
|Initial value=1 / 1
|Applies to=Grid containers
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<grid-line> / <grid-line>
|Description=Specifies the default starting grid column and grid row, respectively.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
This example specifies that (not otherwise placed) grid items
will be placed at column 1, row 2.
*/
#grid{
    grid-auto-position: 1 / 2;
  }
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Grid Layout Module
|URL=http://www.w3.org/TR/css3-grid-layout
|Status=W3C Working Draft
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}