{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add description/notes, compatibility.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>th</code> tag defines a header cell in an HTML table.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableHeaderCellElement
|Tag_omissions=End tag omissable in certain cases
|CSS_display=table-cell
|Content=== Attributes ==

*<code>colspan</code> = valid non-negative integer<br />This attribute gives the number of columns respectively that the cell is to span.
*<code>rowspan</code> = valid non-negative integer<br />This attribute gives the number of rows respectively that the cell is to span. [[#Example_B|[Example B]]]
*<code>headers</code> = unordered set of unique space-separated tokens<br />The value of this attribute must have the value of an id attribute of the th element that is targeted. [[#Example_C|[Example C]]]
*<code>scope</code> = row/ col/ rowgroup/ colgroup<br />The scope attribute specifies the cell which the influence of headding cell reaches. [[#Example_D|[Example D]]]
**row<br />The header cell applies to some of the subsequent cells in the same row(s).
**col<br />The header cell applies to some of the subsequent cells in the same column(s).
**rowgroup<br />The header cell applies to all the remaining cells in the row group. A th element's scope attribute must not be in the row group state if the element is not anchored in a row group.
**colgroup<br />The header cell applies to all the remaining cells in the column group. A th element's scope attribute must not be in the column group state if the element is not anchored in a column group.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[html/elements/table|'''table''']], [[html/elements/td|'''td''']], [[html/elements/thead|'''th''']], and [[html/elements/tr|'''tr''']].
|Code=<nowiki><table>
    <tr>
      <th>
        This text is in the th
      </th>
    </tr>
    <tr>
      <td>
        This text is in the tbody.
      </td>
    </tr>
</table></nowiki>
}}{{Single Example
|Language=HTML
|Description=A table cell referring to the table header
|Code=<nowiki><table>
  <caption>
    <p>table 1. List of HTML elements</p>
  </caption>
  <thead>
    <tr>
      <th id="c1">Number</th>
      <th id="c2">element</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td headers="c1">4.1.1</td>
      <td headers="c2">html</td>
    </tr>
    <tr>
      <td headers="c1">4.2.1</td>
      <td headers="c2">head</td>
    </tr>
  </tbody>
</table></nowiki>
}}{{Single Example
|Language=HTML
|Code=<nowiki><table>
  <caption>
    <p>table 1. List of HTML elements</p>
  </caption>
  <thead>
    <tr>
      <th scope="row">Number</th>
      <th scope="row">element</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4.1.1</td>
      <td>html</td>
    </tr>
    <tr>
      <td>4.2.1</td>
      <td>head</td>
    </tr>
  </tbody>
</table></nowiki>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/tabular-data.html#the-th-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-th-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/tables.html#edef-TH
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