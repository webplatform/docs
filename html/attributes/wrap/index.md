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
|Description=This example dynamically sets the '''wrap''' property of a '''textArea''' to the value selected by the user.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wrap.htm
|Code=
&lt;SCRIPT&gt;
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
To detect the difference between '''soft''' and '''hard''' you must submit the content within the '''textArea''' to an HTTP server.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>textArea</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}