{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example demonstrates how to use the '''setActive''' method between '''frame'''s.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive.htm
|Code=
...
&lt;SCRIPT&gt;
function fnBottomActive(){
    //Set the object with ID{{=}}btnLarger active in frame with ID{{=}}oFrame1.
    window.parent.oFrame1.secondButton.setActive();
}
&lt;/SCRIPT&gt;
...
}}
{{Single_Example
|Description=This example demonstrates how to use the '''setActive''' method between windows. By clicking the '''SetActive''' button in the left window, the method sets the '''Second Button''' as the active object in the right window, although the object does not receive focus. The object receives focus when its page receives focus. To confirm that the object is active, click the right window's title bar. The button appears to be selected.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive_2.htm
|Code=
&lt;HTML&gt;
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''setActive''' method does not cause the document to scroll to the active object in the current page or in another '''frame''' or '''window'''.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>article</code>
*<code>aside</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>bgSound</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>comment</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>figcaption</code>
*<code>figure</code>
*<code>font</code>
*<code>footer</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>header</code>
*<code>hgroup</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>mark</code>
*<code>marquee</code>
*<code>menu</code>
*<code>nav</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>section</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>wbr</code>
*<code>xml</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}