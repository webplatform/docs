{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''CELLSPACING''' attribute and the '''cellSpacing''' property to change the spacing between two cells.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cellSpacing.htm
|Code=
&lt;TABLE ID{{=}}oTable BORDER CELLSPACING{{=}}10&gt;
    &lt;TR&gt;
        &lt;TD&gt;Cell 1&lt;/TD&gt;
        &lt;TD&gt;Cell 2&lt;/TD&gt;
    &lt;/TR&gt;
&lt;/TABLE&gt;
:
&lt;BUTTON onclick{{=}}"oTable.cellSpacing{{=}}20"&gt;Larger spacing&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oTable.cellSpacing{{=}}5"&gt;Smaller spacing&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 11.3.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
*<code>[[html/attributes/cellPadding|cellPadding]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}