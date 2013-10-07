{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Retrieves a collection of all cells in the table row or in the entire table.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''CELLSPACING''' attribute and the '''cellSpacing''' property to change the spacing between two cells.
|Code=&lt;table id{{=}}"oTable" border="0" cellspacing{{=}}"10"&gt;
    &lt;tr&gt;
        &lt;td&gt;Cell 1&lt;/td&gt;
        &lt;td&gt;Cell 2&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
:
&lt;button onclick{{=}}"oTable.cellSpacing{{=}}20"&gt;Larger spacing&lt;/button&gt;
&lt;button onclick{{=}}"oTable.cellSpacing{{=}}5"&gt;Smaller spacing&lt;/button&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cellSpacing.htm
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
*<code>[[html/attributes/cellPadding|cellPadding]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}