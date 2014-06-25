{{Page_Title|grid-area}}
{{Flags
|State=In Progress
|Editorial notes=Add description, compatibility.
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Lays out one or more grid items bound by 4 grid lines. Shorthand for setting [[css/properties/grid-column-start|grid-column-start]], [[css/properties/grid-column-end|grid-column-end]], [[css/properties/grid-row-start|grid-row-start]], and [[css/properties/grid-row-end|grid-row-end]] in a single declaration.}}
{{CSS Property
|Initial value=See individual properties
|Applies to=Grid items
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS percentages=See individual properties
|Values={{CSS Property Value
|Data Type=<grid-line> [ <grid-line> [ <grid-line> [ <grid-line> ] ] ]
|Description=The resolution order of values for this shorthand is grid-row-start, grid-column-start, grid-row-end, grid-column-end. That is, if four <grid-line> values are specified, grid-row-start is set to the first value, grid-column-start is set to the second value, grid-row-end is set to the third value, and grid-column-end is set to the fourth value.

When grid-column-end is omitted, if grid-column-start is an <ident>, grid-column-end is set to that <ident>; otherwise, it is set to auto.

When grid-row-end is omitted, if grid-row-start is an <ident>, grid-row-end is set to that <ident>; otherwise, it is set to auto.

When grid-column-start is omitted, if grid-row-start is an <ident>, all four longhands are set to that value. Otherwise, it is set to auto.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=grid-area: 1 2 2 3;

/*  Equivalent to :

grid-row-start: 1
grid-column-start: 2
grid-row-end: 2;
grid-column-end: 3;

*/
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