{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/objects/Event
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
|Description=This example invokes the '''releaseCapture''' method on the document object.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/releaseCaptureEX.htm
|Code=
&lt;BODY onload{{=}}"oOwnCapture.setCapture();" 
    onclick{{=}}"document.releaseCapture();"&gt;
&lt;DIV ID{{=}}oOwnCapture
    onmousemove{{=}}"oWriteLocation.value {{=}} 
        event.clientX + event.clientY";
    onlosecapture{{=}}"alert(event.srcElement.id + 
        ' has lost mouse capture.')"&gt;
&lt;TEXTAREA ID{{=}}oWriteLocation COLS{{=}}2&gt;&lt;/TEXTAREA&gt;
&lt;/DIV&gt;
&lt;HR&gt;
&lt;DIV ID{{=}}oNoCapture&gt;
&lt;P&gt;Click the document to invoke the releaseCapture method.&lt;/P&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
For '''releaseCapture''' to have an effect, you must set mouse capture through the [[dom/methods/setCapture|'''setCapture''']] method.
You can invoke the '''releaseCapture''' method on the [[dom/document|'''document''']] object. The '''releaseCapture''' method makes it unnecessary to determine which element has capture to programmatically release it. Other actions that release document capture include displaying a modal dialog box and switching focus to another application or browser window.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>custom</code>
*<code>dd</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/document|document]]</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>hn</code>
*<code>hr</code>
*<code>i</code>
*<code>img</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}text</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>s</code>
*<code>samp</code>
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
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/events/losecapture|onlosecapture]]</code>
*<code>[[dom/methods/setCapture|setCapture]]</code>
*<code>[[dom/methods/msSetPointerCapture|msSetPointerCapture]]</code>
*<code>[[dom/methods/msReleasePointerCapture|msReleasePointerCapture]]</code>
*<code>Conceptual</code>
*<code>About Mouse Capture</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}