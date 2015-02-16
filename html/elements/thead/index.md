{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Should have automatic child links generated.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''thead''' element  (&lt;thead&gt;) identifies header rows at the top of a table, usually containing column labels.  It may contain one or more rows of &lt;th&gt; or &lt;td&gt; cells.  If it only contains a single row the child &lt;tr&gt; tag may be omitted.|The <code>thead</code> tag is used to group header content in an HTML table_ Generally with have th tags with attribute of scope="col"
}}
{{Markup_Element
|DOM_interface=dom/HTMLTableSectionElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example uses the ''thead''' element and the [[html/elements/table|'''table''']], [[html/elements/tbody|'''tbody''']], [[html/elements/td|'''td''']], and [[html/elements/tr|'''tr''']] elements to create a table that includes the first row in the table header and the second row in the table body.
|Code=&lt;table&gt;
&lt;thead&gt;
  &lt;tr&gt;
    &lt;th scope="col"&gt;Player&lt;/th&gt;
    &lt;th scope="col"&gt;Position&lt;/th&gt;
  &lt;/tr&gt;
&lt;/thead&gt;
&lt;tbody&gt;
  &lt;tr&gt;
    &lt;td&gt;James, Lebron&lt;/td&gt;
    &lt;td&gt;SF&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Wade, Dwayne&lt;/td&gt;
    &lt;td&gt;SG&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Bosh, Chris&lt;/td&gt;
    &lt;td&gt;PF&lt;/td&gt;
  &lt;/tr&gt;
&lt;/tbody&gt;
&lt;/table&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Valid tags within the '''THEAD''' element include:
*'''td''' * chances are should be a th not a td, and scope of column
*'''th'''
*'''tr'''

You can specify only one '''thead''' object specified for any given [[html/elements/table|'''table''']] object.
The [[html/elements/table|'''table''']] object and its associated elements have a separate table object model, which uses different methods than the general object model.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 11.2.3



 
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-thead-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-thead-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-THEAD
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}