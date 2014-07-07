{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, compatibility, general discussion
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
|Description=The following example shows how to use the '''isDisabled''' property to determine whether an object is disabled.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
function chgInput() {
    currentState {{=}} oTextInput.isDisabled;
    newState {{=}} !currentState;
    oTextInput.disabled {{=}} newState;
    oCurrentValue.innerText {{=}} newState;
    newState{{=}}{{=}}true ? oBtn.innerText{{=}}"Enable" : oBtn.innerText{{=}}"Disable"
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"oCurrentValue.innerText {{=}} oTextInput.isDisabled;"&gt;
&lt;P&gt;Click the button to enable or disable the &lt;B&gt;INPUT&lt;/B&gt;.&lt;/P&gt;
&lt;P&gt;
&lt;INPUT ID{{=}}"oBtn" TYPE{{=}}"button" VALUE{{=}}"Disable" onclick{{=}}"chgInput()" /&gt;
&lt;/P&gt;
&lt;P&gt;&lt;INPUT ID{{=}}"oTextInput" VALUE{{=}}"This is some text." /&gt;&lt;/P&gt;
Input disabled: &lt;SPAN ID{{=}}"oCurrentValue"&gt;&lt;/SPAN&gt;
&lt;/BODY&gt;
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