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
|Description=This example uses the '''COLS''' attribute and the '''cols''' property to set the number of columns in HTML and retrieve the number of columns in script.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cols.htm
|Code=
&lt;SCRIPT&gt;
function checkCols(oObject)
{
    var iColumns {{=}} oObject.cols;
    alert (iColumns);
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE ID{{=}}oTable BORDER COLS{{=}}3 onclick{{=}}"checkCols(this)"&gt;
&lt;TR&gt;&lt;TD&gt;Column 1&lt;/TD&gt;&lt;TD&gt;Column 2&lt;/TD&gt;&lt;TD&gt;Column 3&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Specifying this number can speed up the processing of the table.
Windows Internet Explorer 8 will only render tables up to 1000 columns. To force Windows Internet Explorer 7 rendering mode, see How Do I Take Advantage of the New Features in Internet Explorer 8.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}