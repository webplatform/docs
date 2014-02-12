{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''canHaveHTML''' property to determine whether an object can contain HTML markup.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function answer(arg) {
    arg ? alert("Yes") : alert("No");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;INPUT: &lt;INPUT type{{=}}"text" ID{{=}}"oInput" VALUE{{=}}"oInput" /&gt;&lt;/P&gt;
&lt;P&gt;SPAN: &lt;SPAN ID{{=}}"oSpan"&gt;oSpan&lt;/SPAN&gt;&lt;/P&gt;
&lt;BUTTON onclick{{=}}"answer(oInput.canHaveHTML);"&gt;
Can the INPUT contain HTML?
&lt;/BUTTON&gt;&amp;nbsp;
&lt;BUTTON onclick{{=}}"answer(oSpan.canHaveHTML);"&gt;
Can the SPAN contain HTML?
&lt;/BUTTON&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/canHaveHTML.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The property is read-only for all objects except the following, for which it is read-write: [[dom/defaultSelected|'''defaults''']].
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}