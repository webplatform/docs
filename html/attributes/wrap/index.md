{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add Summary
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example dynamically sets the '''wrap''' property of a '''textArea''' to the value selected by the user.
|Code=&lt;SCRIPT&gt;
function ChangeWrap(oSelect, oTA)
{
    cValue {{=}} oSelect.options(oSelect.selectedIndex).value;
    oTA.wrap {{=}} cValue;
}
&lt;/SCRIPT&gt;
...
&lt;SELECT ID{{=}}cboWrap onchange{{=}}"ChangeWrap(this, txt1)"&gt;
&lt;OPTION VALUE{{=}}soft&gt;soft
&lt;OPTION VALUE{{=}}hard&gt;hard
&lt;OPTION VALUE{{=}}off&gt;off
&lt;/SELECT&gt;
&lt;P&gt;
&lt;TEXTAREA ID{{=}}txt1 STYLE{{=}}"height:200;width:200"&gt;&lt;/TEXTAREA&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wrap.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
To detect the difference between '''soft''' and '''hard''' you must submit the content within the '''textArea''' to an HTTP server.
|Import_Notes====Syntax===
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
*<code>textArea</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}