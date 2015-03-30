{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add description/notes, compatibility.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>tfoot</code> tag is used to group footer content in an HTML table.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableSectionElement
|Tag_omissions=End tag omissable in certain cases
|CSS_display=table-footer-group
|Content=The &lt;tfoot&gt; element represents the block of rows that consist of the column summaries (footers) for the parent table element, if the tfoot element has a parent and it is a table.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example uses the '''tfoot''' element and the [[html/elements/table|'''table''']], [[html/elements/tbody|'''tbody''']], [[html/elements/td|'''td''']], and [[html/elements/tr|'''tr''']] elements to create a table that includes the first row in the table body and the second row in the table footer.
|Code=<nowiki><table>
<tbody>
  <tr>
    <td>
     This text is in the table body.
    </td>
  </tr>
</tbody>
<tfoot>
  <tr>
    <td>
       This text is in the table footer.
    </td>
  </tr>
</tfoot>
</table></nowiki>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-tfoot-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-tfoot-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-TFOOT
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Tables
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}