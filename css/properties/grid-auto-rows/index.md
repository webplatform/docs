{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|When a grid item is placed into a row or column that is not explicitly sized (by [[css/properties/grid-template-rows|grid-template-rows]] or [[css/properties/grid-template-columns|grid-template-columns]]), implicit grid tracks are created to hold it. This property (with [[css/properties/grid-auto-columns|grid-auto-columns]]) specifies the size of such implicitly-created tracks.}}
{{CSS Property
|Initial value=auto
|Applies to=Grid containers
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=As specified
|Values={{CSS Property Value
|Data Type=<track-size>
|Description=A space-separated track list specifying the line names and track sizing functions of the grid. See [http://www.w3.org/TR/css3-grid-layout/#track-sizing track sizing] in specification for details.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
In this example, grid item B is positioned in column 5, 
which creates four implicit columns (1-4) and one implicit row (2). 
The implicit (auto) columns and rows are sized at 20px
using grid-auto-columns and grid-column-rows.
*/
<style type="text/css">
  #grid { 
display: grid; 
grid-auto-columns: 20px; 
grid-auto-rows: 20px }
  #A { grid-column: 1;          grid-row: 1; }
  #B { grid-column: 5;          grid-row: 1 / span 2; }
  #C { grid-column: 1 / span 2; grid-row: 2; }
</style>
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
{{See_Also_Section
|Topic_clusters=CSS Layout, Grid Layout
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}