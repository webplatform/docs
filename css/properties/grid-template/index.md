{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, compatibility.
|Checked_Out=No
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Shorthand for setting [[css/properties/grid-template-columns|grid-template-columns]], [[css/properties/grid-template-rows|grid-template-rows]], and [[css/properties/grid-template-areas|grid-template-areas]] in a single declaration.}}
{{CSS Property
|Initial value=See individual properties
|Applies to=Grid containers
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS percentages=See indvidual properties
|Values={{CSS Property Value
|Data Type=none
|Description=Sets all three individual properties to their initial values ("none").
}}{{CSS Property Value
|Data Type=<grid-template-columns> / <grid-template-rows>
|Description=Sets grid-template-columns and grid-template-rows to the specified values, and sets grid-template-areas to "none".
}}{{CSS Property Value
|Data Type=<track-list> / <line-names> <string> <track-size> <line-names>
|Description=Sets grid-template-columns to the track listing specified before the slash (or "none", if not specified). Sets grid-template-areas to the strings listed after the slash. Sets grid-template-rows to the <track-size>s following each string (filling in "auto" for any missing sizes), and splicing in the named lines defined before/after each size.

This syntax allows the author to align track names and sizes inline with their respective grid areas.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
The shorthand syntax
*/
grid-template: auto 1fr auto / auto 1fr;
/*
is equivalent to
*/
grid-template-columns: auto 1fr auto;
grid-template-rows: auto 1fr;
grid-template-areas: none;
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