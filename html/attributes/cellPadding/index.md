{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies the space, in pixels, between the cell wall and the cell content. Not supported in HTML5. Use CSS.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=The <table> cellpadding attribute is not supported in HTML5. Use CSS instead.

The cellpadding attribute specifies the space, in pixels, between the cell wall and the cell content.

Note: Do not confuse this with the cellspacing attribute, which specifies the space between cells.

Tip: It may be better to NOT specify a cellpadding, and use CSS to apply padding instead.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<table border="1" cellpadding="10">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>0</td>
  </tr>
</table>
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 11.3.3
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
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
*<code>[[html/attributes/cells|cellSpacing]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}