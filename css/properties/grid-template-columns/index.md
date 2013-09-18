{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies (with [[css/properties/grid-template-rows|grid-template-rows]]) the line names and track sizing functions of the grid. Each sizing function can be specified as a length, a percentage of the grid container’s size, a measurement of the contents occupying the column or row, or a fraction of the free space in the grid.}}
{{CSS Property
|Initial value=none
|Applies to=grid containers
|Inherited=No
|Media=visual
|Computed value=As specified, except for "auto"
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Indicates that there is no explicit grid; any rows/columns will be implicitly generated, and their size will be determined by the grid-auto-rows and grid-auto-columns properties.
}}{{CSS Property Value
|Data Type=<track-list>
|Description=Specifies the track list for the grid columns. See [http://www.w3.org/TR/css3-grid-layout/#track-list specification] for complete syntax.
}}{{CSS Property Value
|Data Type=subgrid <line-name-list>
|Description=Indicates that the grid will align to its parent grid in that axis. Rather than specifying the sizes of rows/columns explicitly, they will be taken from the parent grid’s definition. If the grid container is not a grid item, this value computes to "none".
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=grid-template-columns: 100px 1fr max-content minmax(min-content, 1fr);
/* Creates five grid lines:
1. At the start edge of the grid container
2. 100px from the start edge of the grid container
3. At a distance from the previous line equal to half the free space 
   (the width of the grid container minus the width of the non-flexible grid tracks)
4. At a distance from the previous line equal to the maximum size of any grid items 
   belonging to the column between these two lines
5. At a distance from the previous line at least as large as the largest minimum size of any grid items 
   belonging to the column between these two lines, but no larger than the other half of the free space
*/
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Grid Layout Module Level 1
|URL=http://www.w3.org/TR/css3-grid-layout/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=Yes
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