{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Event}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the [[dom/clipboardData|'''clipboardData''']] object to implement custom editing functionality.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;
var sNewString {{=}} "new content associated with this object";
var sSave {{=}} "";
// Selects the text that is to be cut.
function fnLoad() {
    var r {{=}} document.body.createTextRange();
    r.findText(oSource.innerText);
    r.select();
}
// Stores the text of the SPAN in a variable that is set 
// to an empty string in the variable declaration above.
function fnBeforeCut() {
    sSave {{=}} oSource.innerText;
    event.returnValue {{=}} false;
}
// Associates the variable sNewString with the text being cut.
function fnCut() {
    window.clipboardData.setData("Text", sNewString);
}
function fnBeforePaste() {
    event.returnValue {{=}} false;
}
// The second parameter set in getData causes sNewString 
// to be pasted into the text input. Passing no second
// parameter causes the SPAN text to be pasted instead.
function fnPaste() {
    event.returnValue {{=}} false;
    oTarget.value {{=}} window.clipboardData.getData("Text", sNewString);
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"fnLoad()"&gt;
&lt;SPAN ID{{=}}"oSource" 
      onbeforecut{{=}}"fnBeforeCut()" 
      oncut{{=}}"fnCut()"&gt;Cut this Text&lt;/SPAN&gt;
&lt;INPUT ID{{=}}"oTarget" TYPE{{=}}"text" VALUE{{=}}"Paste the Text Here"
      onbeforepaste{{=}}"fnBeforePaste()" 
      onpaste{{=}}"fnPaste()"&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Creating custom code to enable the Paste command requires several steps.
#Set the event object [[dom/properties/returnValue|'''returnValue''']] to false in the [[dom/events/beforepaste|'''onbeforepaste''']] event to enable the Paste shortcut menu item.
#Cancel the default behavior of the client by setting the event object [[dom/properties/returnValue|'''returnValue''']] to false in the '''onpaste''' event handler. This applies only to objects, such as the '''text box''', that have a default behavior defined for them.
#Specify a data format in which to paste the selection through the [[dom/methods/getData|'''getData''']] method of the [[dom/clipboardData|'''clipboardData''']] object.
#Invoke the method in the '''onpaste''' event to execute custom paste code.

Inserts the data from the system clipboard into the specified location on the document.
To invoke this event, do one of the following:
*Right-click to display the shortcut menu and select Paste.
*Or press CTRL+V.

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
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
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
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>ol</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>rt</code>
*<code>ruby</code>
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
*<code>[[dom/methods/getData|getData]]</code>
*<code>[[dom/events/beforecopy|onbeforecopy]]</code>
*<code>[[dom/events/beforecut|onbeforecut]]</code>
*<code>[[dom/events/beforepaste|onbeforepaste]]</code>
*<code>oncopy</code>
*<code>[[dom/events/cut|oncut]]</code>
*<code>Conceptual</code>
*<code>About DHTML Data Transfer</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}