{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets the wrap style ('''soft''', '''hard''', or '''off''') for a text element.}}
{{Markup_Attribute
|Applies_to=dom/HTMLElement
|Property_applies_to=dom/HTMLElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example dynamically sets the '''wrap''' property of a '''textArea''' to the value selected by the user.
|Code=&lt;script&gt;
function ChangeWrap(oSelect, oTA)
{
    cValue {{=}} oSelect.options(oSelect.selectedIndex).value;
    oTA.wrap {{=}} cValue;
}
&lt;/script&gt;
...
&lt;select id{{=}}cboWrap onchange{{=}}"ChangeWrap(this, txt1)"&gt;
&lt;option value{{=}}soft&gt;soft
&lt;option value{{=}}hard&gt;hard
&lt;option value{{=}}off&gt;off
&lt;/select&gt;
&lt;p&gt;
&lt;textarea id{{=}}txt1 style{{=}}"height:200;width:200"&gt;&lt;/textarea&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wrap.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
To detect the difference between '''soft''' and '''hard''' you must submit the content within the '''textArea''' to an HTTP server.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}