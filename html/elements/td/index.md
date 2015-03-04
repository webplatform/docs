{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add description/notes, compatibility.
|Checked_Out=No
|Content=Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Defines a standard Cell in an HTML table.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableDataCellElement
|Tag_omissions=Closing tag omissible in certain cases
|CSS_display=table-cell
|Content=== Attributes ==
*<code>colspan</code> = valid non-negative integer<br />This attribute gives the number of columns respectively that the cell is to span.
*<code>rowspan</code> = valid non-negative integer<br />This attribute gives the number of rows respectively that the cell is to span.
*<code>headers</code> = unordered set of unique space-separated tokens<br />The value of this attribute must have the value of an id attribute of the th element that is targeted.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[html/elements/table|'''table''']] element with [[html/elements/tr|'''tr''']] and [[html/elements/td|'''td''']] to create a table with three rows and two columns.
|Code=&lt;table border{{=}}"1" width{{=}}"80%"&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;Row 1, Column 1 text.&lt;/td&gt;
      &lt;td&gt;Row 1, Column 2 text.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;Row 2, Column 1 text.&lt;/td&gt;
      &lt;td&gt;Row 2, Column 2 text.&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-td-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-td-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-TD
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Tables
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}