{{Page_Title|grid-row}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets or sets a value that indicates which row child content within a Grid should appear in.  Shorthand for setting [[css/properties/grid-row-start|grid-row-start]] and [[css/properties/grid-row-end|grid-row-end]] in a single declaration.}}
{{CSS Property
|Initial value=See individual properties
|Applies to=Grid items
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS percentages=See individual properties
|Values={{CSS Property Value
|Data Type=<grid-line> [ / <grid-line> ]
|Description=If two <grid-line> values are specified, the grid-row-start property is set to the value before the slash, and the grid-row-end property is set to the value after the slash. 

When the second value is omitted, then if the first value is an identifier (<ident>), the grid-row-end property is also set to that <ident>; otherwise, it is set to "auto".
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
The shorthand syntax
*/
grid-row: 1 / 3;
/*
is equivalent to
*/
grid-row-start: 1
grid-row-end: 3;
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