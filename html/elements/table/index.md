{{Page_Title|table}}
{{Flags
|State=Not Ready
|Editorial notes=Add description, notes, compatibility.
|Checked_Out=Yes
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>&lt;table&gt;</code> element is a wrapper for an HTML table. It defines the start and end of a table, and can contain other table elements, such as <code>&lt;tr&gt;</code>.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableElement
|Tag_omissions=
|CSS_display=
|Content=The <code>&lt;table&gt;</code> element is a container for HTML table data, which is used to mark up tabular data. Tabular data is any data that can be systematically displayed in rows and columns, for example, "See table 3 for an example."

Tables were often used for laying out web pages because tables helped fix the position of text on the page, however, this use has become an outdated.  We recommend you use <code>&lt;div&gt;</code> and <code>&lt;span&gt;</code> for fixed layouts. You can still use tables for tabular data. 

You might find working with an HTML table editor easier than coding tables by hand, unless you are especially adept at visualizing table row and columns using the appropriate HTML tags. It is easy to miss or drop a tag when coding tables manually, which will cause your table to be malformed.  
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[html/elements/tbody|'''tbody''']] element with the [[html/elements/table|'''table''']], [[html/elements/td|'''td''']], [[html/elements/thead|'''thead''']], and [[html/elements/tr|'''tr''']] elements to create a table with the first row in the table head and the second row in the table body.
|Code=&lt;table&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;td&gt;
        This text is in the thead.
      &lt;/td&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;
        This text is in the tbody.
      &lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=At the most simple level you need to use the following three groups of tags to create a basic table. 

1) <table></table>
<table> tag begins the table, and <ltable> tag ends the table.

2> <tr</tr>
<tr> creates a row while </tr> ends the row. 

3> <td></td>
<td> creates a column space while </td> ends the column space. These are usually nested inside a pair of <tr></tr> tags. The term "td" stands for table data, but as a representation, you can view it like a "column tag".

The three pairs of tags can create a simple two row, two column table using the code below. 

<table>
<tr><td>row 1 col 1</td><td>row 1 col 2</td></tr>
<tr><td>row 1 col 2</td><td>row 2 col 2</td></tr>
</table>
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-table-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-table-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-TABLE
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