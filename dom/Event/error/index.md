{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''onerror''' event to handle run-time script errors and object load errors.

The following example specifies an invalid script entry. The script in the text field is evaluated when the Throw Error button is clicked. The '''onerror''' event fires because the script is invalid. The error results are inserted at the bottom of the sample page instead of in a dialog box.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX.htm
|Code=
&lt;script&gt;
window.onerror{{=}}fnErrorTrap;
function fnErrorTrap(sMsg,sUrl,sLine){
   oErrorLog.innerHTML{{=}}"&lt;b&gt;An error was thrown and caught.&lt;/b&gt;&lt;br /&gt;";
   oErrorLog.innerHTML+{{=}}"Error: " + sMsg + "&lt;br /&gt;";
   oErrorLog.innerHTML+{{=}}"Line: " + sLine + "&lt;br /&gt;";
   oErrorLog.innerHTML+{{=}}"URL: " + sUrl + "&lt;br /&gt;";
   return false;
}
function fnThrow(){
   eval(oErrorCode.value);
}
&lt;/script&gt;
&lt;input type{{=}}"text" id{{=}}"oErrorCode" value{{=}}"someObject.someProperty{{=}}true;"/&gt;
&lt;input type{{=}}"button" value{{=}}"Throw Error" onclick{{=}}"fnThrow()"/&gt;
&lt;br /&gt;
&lt;div id{{=}}"oErrorLog"&gt;&lt;/div&gt;
}}
{{Single_Example
|Description=The following example shows how to set the handler for the '''onerror''' event in script before an image source is specified. When the invalid source is set on the '''img''' element, the event fires.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX1.htm
|Code=
&lt;script&gt;
var sImg{{=}}'&lt;img style{{=}}"display: none;" id{{=}}"oStub" alt{{=}}"Default Text"/&gt;';
function fnLoadFirst(){
   oContainer.innerHTML{{=}}sImg;
   oStub.onerror{{=}}fnLoadFail1;
   oStub.src{{=}}"";
   oStub.style.display{{=}}"block";
}
function fnLoadFail1(){
   oStub.alt{{=}}"Image failed to load.";
   return true;
}
&lt;/script&gt;
&lt;input type{{=}}"button" value{{=}}"Load First Image" onclick{{=}}"fnLoadFirst()"/&gt;
&lt;div id{{=}}oContainer&gt;&lt;/div&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
To suppress the default Windows Internet Explorer error message for the '''window''' event, set the [[dom/properties/returnValue|'''returnValue''']] property of the '''event''' object to '''true''' or simply return <code>true</code> in Microsoft JScript.
The '''onerror''' event fires for run-time errors, but not for compilation errors. In addition, error dialog boxes raised by script debuggers are not suppressed by returning <code>true</code>. To turn off script debuggers, disable script debugging in Internet Explorer by choosing  '''Internet Options''' from the '''Tools''' menu. Click the '''Advanced''' tab and select the appropriate check box(es).
Displays the browser error message when a problem occurs and executes any error handling routine associated with the event.
To invoke this event, do one of the following:
*Run-time script error, such as an invalid object reference or security violation.
*Error while downloading an object, such as an image.
*Windows Internet Explorer 9. An error occurs while fetching media data.

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLAnchorEvents2'''
*'''HTMLAreaEvents2'''
*'''HTMLButtonElementEvents2'''
*'''HTMLControlElementEvents2'''
*'''HTMLDocumentEvents2'''
*'''HTMLElementEvents2'''
*'''HTMLFormElementEvents2'''
*'''HTMLImgEvents2'''
*'''HTMLFrameSiteEvents2'''
*'''HTMLInputFileElementEvents2'''
*'''HTMLInputImageEvents2'''
*'''HTMLInputTextElementEvents2'''
*'''HTMLLabelEvents2'''
*'''HTMLLinkElementEvents2'''
*'''HTMLMapEvents2'''
*'''HTMLMarqueeElementEvents2'''
*'''HTMLObjectElementEvents2'''
*'''HTMLOptionButtonElementEvents2'''
*'''HTMLScriptEvents2'''
*'''HTMLSelectElementEvents2'''
*'''HTMLStyleElementEvents2'''
*'''HTMLTableEvents2'''
*'''HTMLTextContainerEvents2'''
*'''HTMLWindowEvents2'''
*'''HTMLDocumentEvents4'''
*'''HTMLElementEvents4'''

|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

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
*<code>audio</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>bgSound</code>
*<code>big</code>
*<code>body</code>
*<code>blockQuote</code>
*<code>br</code>
*<code>button</code>
*<code>[[canvas/objects/canvas|canvas]]</code>
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
*<code>[[dom/Document|Document]]</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
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
*<code>marquee</code>
*<code>[[html/elements/media|media]]</code>
*<code>menu</code>
*<code>meta</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>object</code>
*<code>ol</code>
*<code>optGroup</code>
*<code>option</code>
*<code>p</code>
*<code>param</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>select</code>
*<code>small</code>
*<code>source</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>style</code>
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
*<code>video</code>
*<code>window</code>
*<code>xmp</code>
*<code>[[dom/events/errorupdate|onerrorupdate]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}