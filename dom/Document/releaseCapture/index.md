{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Removes mouse capture from the object in the current document.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Document
|Example_object_name=document
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example invokes the '''releaseCapture''' method on the document object.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;&lt;/title&gt;
 &lt;/head&gt;
 &lt;body onload{{=}}"oOwnCapture.setCapture();" 
    onclick{{=}}"document.releaseCapture();"&gt;
  &lt;div id{{=}}"oOwnCapture"
    onmousemove{{=}}"oWriteLocation.value {{=}} 
        event.clientX + event.clientY";
    onlosecapture{{=}}"alert(event.srcElement.id + 
        ' has lost mouse capture.')"&gt;
  &lt;textarea id{{=}}"oWriteLocation" cols{{=}}"2"&gt;&lt;/textarea&gt;
  &lt;/div&gt;
  &lt;hr/&gt;
  &lt;div id{{=}}oNoCapture&gt;
   &lt;p&gt;Click the document to invoke the releaseCapture method.&lt;/p&gt;
  &lt;/div&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/releaseCaptureEX.htm
}}
}}
{{Notes_Section
|Notes=*For '''releaseCapture''' to have an effect, you must set mouse capture through the [[dom/methods/setCapture|'''setCapture''']] method.
*You can invoke the '''releaseCapture''' method on the [[dom/Document|'''Document''']] object.
*The '''releaseCapture''' method makes it unnecessary to determine which element has capture to programmatically release it.
*Other actions that release document capture include displaying a modal dialog box and switching focus to another application or browser window.
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
*<code>[[dom/Document|Document]]</code>
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}