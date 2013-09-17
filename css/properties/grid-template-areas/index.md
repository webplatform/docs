{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies named grid areas which are not associated with any particular grid item, but can be referenced from the grid-placement properties. The syntax of the grid-template-areas property also provides a visualization of the structure of the grid, making the overall layout of the grid container easier to understand.}}
{{CSS Property
|Initial value=none
|Applies to=Grid containers
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=The grid container does not define any named grid areas.
}}{{CSS Property Value
|Data Type=<string>
|Description=A row is created for every separate string listed, and a column is created for each identifier or period (".") in the string. A period represents an unnamed area in the grid container. An identifier creates a named grid area with the identifier as its name.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* 
Creates a page layout where areas are defined for header content (head), 
navigational content (nav), footer content (foot), and main content (main). 
Accordingly, the template creates three rows and two columns, with four named grid areas. 
The head area spans both columns and the first row of the grid.
*/

<style type="text/css">
  #grid {
    display: grid;
    grid-template-areas: "head head"
                         "nav  main"
                         "foot .   "
  }
  #grid > header { grid-area: head; }
  #grid > nav    { grid-area: nav; }
  #grid > main   { grid-area: main; }
  #grid > footer { grid-area: foot; }
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