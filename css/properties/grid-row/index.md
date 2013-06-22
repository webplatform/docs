{{Page_Title|grid-row}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Needs Review
|Content=Compatibility Incomplete, Examples Needed, Needs Summary
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Shorthand for grid-before/after and grid-start/end.}}
{{CSS Property
|Initial value=1
|Applies to=grid items
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=&lt;integer&gt; {{!}}{{!}} &lt;string&gt;
|Description=Integer value or String that identifies the specified row.
}}{{CSS Property Value
|Data Type=span && &lt;integer&gt; {{!}}{{!}} &lt;string&gt;
|Description=Places an item with contiguous space available to the <integer> value. Using the <string> value only considers lines with that name.
}}{{CSS Property Value
|Data Type=auto
|Description=Automatically places an item using the auto-placement algorithm.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Places an element "#label" into the "labels" column on row 3.
|Code=#label {

grid-column: 'labels';
grid-row: 3;

}
}}
}}
{{Notes_Section
|Usage=<code>'''grid-row: '''''
&lt;integer&gt;
''</code>
|Notes====Remarks===
The row numbering system is a 1-based index, with 1 being the default. That is, row numbering does not begin with zero.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/css3-grid-layout/#grid-row CSS Grid Layout]
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
|Topic_clusters=Grid Layout
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}