{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, compatibility, rearrange MSDN content to use WPD sections
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
|Description=The following example shows how to use the '''isMultiLine''' property to determine whether the content of an object can contain only one line or multiple lines of text.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function answer(arg) {
    arg ? alert("Yes") : alert("No");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;INPUT: &lt;INPUT type{{=}}"text" ID{{=}}"oInput" VALUE{{=}}"oInput"/&gt;
&lt;BUTTON onclick{{=}}"answer(oInput.isMultiLine);"&gt;
Can the INPUT contain more than one line?&lt;/BUTTON&gt;
&lt;/P&gt;

&lt;P&gt;TEXTAREA: &lt;TEXTAREA ID{{=}}"oTextarea"&gt;oTextarea&lt;/TEXTAREA&gt;
&lt;BUTTON onclick{{=}}"answer(oTextarea.isMultiLine);"&gt;
Can the TEXTAREA contain more than one line?&lt;/BUTTON&gt;
&lt;/P&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ismultilineEX1.htm
}}
}}
{{Notes_Section
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