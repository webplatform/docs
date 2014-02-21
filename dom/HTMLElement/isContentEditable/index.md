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
|Description=The following example shows how to use the '''isContentEditable''' property to determine whether the user can edit the content of an object.
|Code=&lt;head&gt;
&lt;SCRIPT&gt;
function chgSpan() {
    currentState {{=}} oSpan.isContentEditable;
    newState {{=}} !currentState;
    oSpan.contentEditable {{=}} newState;
    oCurrentValue.innerText {{=}} newState;
    newState{{=}}{{=}}false ? oBtn.innerText{{=}}"Enable Editing" :
        oBtn.innerText{{=}}"Disable Editing"
}
&lt;/SCRIPT&gt;
&lt;/head&gt;
&lt;body onload{{=}}"oCurrentValue.innerText {{=}} oSpan.isContentEditable;"&gt;
&lt;P&gt;Click the button to enable or disable SPAN content editing.&lt;/P&gt;
&lt;P&gt;
&lt;BUTTON ID{{=}}"oBtn" onclick{{=}}"chgSpan()"&gt;Enable Editing&lt;/BUTTON&gt;
&lt;/P&gt;
&lt;P&gt;&lt;SPAN ID{{=}}"oSpan"&gt;You can edit this text.&lt;/SPAN&gt;&lt;/P&gt;
Span can be edited: &lt;SPAN ID{{=}}"oCurrentValue"&gt;&lt;/SPAN&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/editRegions.htm
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