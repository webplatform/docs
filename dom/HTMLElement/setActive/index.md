{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example demonstrates how to use the '''setActive''' method between '''frame'''s.
|Code=...
&lt;SCRIPT&gt;
function fnBottomActive(){
    //Set the object with ID{{=}}btnLarger active in frame with ID{{=}}oFrame1.
    window.parent.oFrame1.secondButton.setActive();
}
&lt;/SCRIPT&gt;
...
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive.htm
}}{{Single Example
|Description=This example demonstrates how to use the '''setActive''' method between windows. By clicking the '''SetActive''' button in the left window, the method sets the '''Second Button''' as the active object in the right window, although the object does not receive focus. The object receives focus when its page receives focus. To confirm that the object is active, click the right window's title bar. The button appears to be selected.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function fnOpen(){
    //Open new window.
    oWin1 {{=}} window.open("/workshop/samples/author/dhtml/refs/setactive_content.htm",
        "oWin1", 
        "top{{=}}10px,left{{=}}480px,height{{=}}375px,width{{=}}200px,resizable{{=}}1");
    //Set focus back to the parent window.
    this.focus();
}    
function fnBottomActive(){
    //Set the object with ID{{=}}btnLarger active in the other window.
    window.parent.oWin1.secondButton.setActive();
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"fnOpen();"&gt;
&lt;CENTER&gt;
&lt;TABLE border{{=}}"1"&gt;
&lt;TR&gt;&lt;TD&gt;
    &lt;BUTTON id{{=}}"btn1" onclick{{=}}"fnBottomActive();"&gt;Set Active&lt;/BUTTON&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/CENTER&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive_2.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''setActive''' method does not cause the document to scroll to the active object in the current page or in another '''frame''' or '''window'''.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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