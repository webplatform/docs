{{Page_Title|grid-row-position}}
{{Flags
|High-level issues=Needs Flags, Needs Topics, Needs Review
|Content=Incomplete, Examples Needed, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifices a row position based on integer location, string value, or desired row size. [grid-row] is used as short-hand.}}
{{CSS Property
|Initial value=1
|Applies to=grid item elements 
|Inherited=No
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
|Examples=
}}
{{Notes_Section
|Usage=<code>'''grid-row-position: '''''
&lt;integer&gt;
''</code>
|Notes====Remarks===
The row numbering system is a 1-based index, with 1 being the default. That is, row numbering does not begin with zero.
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