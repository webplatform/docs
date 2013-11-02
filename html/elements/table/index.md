{{Page_Title|table}}
{{Flags
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>&lt;table&gt;</code> element is a wrapper for an HTML table. It defines the start and end of a table, and as such can contain other table elements, such as <code>&lt;tr&gt;</code>.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableElement
|Content=The <code>&lt;table&gt;</code> element is a container for HTML tables, which are used to markup tabular data.

Tables are also often used for laying out web pages, but this is a bad practice that should not be done anymore. Use <code>&lt;div&gt;</code> and <code>&lt;span&gt;</code> instead.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''TABLE''' element with '''THEAD''', '''TR''', and '''TH''' to create a table with three rows and two columns.
|Code=&lt;table border{{=}}"1" width{{=}}"80%"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th&gt;Heading 1&lt;/th&gt;
      &lt;th&gt;Heading 2&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
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
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/html/wg/drafts/html/master/tabular-data.html#the-table-element
|Status=Editor's Draft
}}{{Related Specification}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML, Tables
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}