{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=none
|Applies to=none
|Inherited=No
|Media=visual
|Computed value=As specified, except for ‘auto’ (see prose)
|Animatable=No
|CSS object model property=gridDefinitionColumns
|CSS percentages=n/a
|Values={{CSS Property Value
|Data Type=none
|Description=No initial grid; any rows/columns will be implicitly generated, and their size will be determined by the ‘grid-auto-rows’ and ‘grid-auto-columns’ properties.
}}{{CSS Property Value
|Data Type=<track-list>
|Description=* &lt;length&gt;
* &lt;percentage&gt;: Percentage values are relative to the measure (logical width) of the grid container in grid column tracks, and the extent (logical height) of the grid container in grid row tracks. If the measure or extent of the grid container is an indefinite size, <percentage> values relative to that size are treated as ‘auto’.
* &lt;flex&gt;: A non-negative dimension with the unit "fr". Each <flex> value takes a share of the remaining space in proportion to its value. See Flexible Lengths for more details.
* max-content: Represents the largest max size contribution of the grid items occupying the grid track.
* min-content: Represents the largest min size contribution of the grid items occupying the grid track.
* minmax(min, max): Defines a size range greater than or equal to min and less than or equal to max. If max < min, then max is ignored and ‘minmax(min,max)’ is treated as min.
* auto: Computes to ‘minmax(min-content, max-content)’.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
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
|Topic_clusters=CSS Layout, Grid Layout
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}