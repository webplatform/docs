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
|Description=This example uses the [[dom/methods/setData|'''setData''']] and [[dom/methods/getData|'''getData''']] methods with the [[dom/clipboardData|'''clipboardData''']] object to perform a cut-and-paste operation through the shortcut menu.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm
|Code=
&lt;head&gt;
&lt;script&gt;
var sSave {{=}} "";
function fnBeforeCut() {
   event.returnValue {{=}} false;
}
function fnCut() {
   event.returnValue {{=}} false;
   sSave {{=}} oSource.innerText;
   oSource.innerText {{=}} "";
}
function fnBeforePaste() {
   event.returnValue {{=}} false;
}
function fnPaste() {
   event.returnValue {{=}} false;
   oTarget.innerText {{=}} sSave;
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div id{{=}}"oSource" class{{=}}"selectandcut" 
    onbeforecut{{=}}"fnBeforeCut()" 
    oncut{{=}}"fnCut()"&gt;Select and Cut this Text 
&lt;/div&gt;
&lt;br&gt;
&lt;br&gt;
&lt;div id{{=}}"oTarget" class{{=}}"pastehere" 
    onbeforepaste{{=}}"fnBeforePaste()" 
    onpaste{{=}}"fnPaste()"&gt;Paste the Text Here 
&lt;/div&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Creating custom code for cutting requires several steps:
#Set '''event.returnValue{{=}}false''' in the '''onbeforecut''' event to enable the Cut shortcut menu item.
#Specify a data format in which to transfer the selection through the [[dom/methods/setData|'''setData''']] method of the [[dom/clipboardData|'''clipboardData''']] object.
#Invoke the [[dom/methods/setData|'''setData''']] method in the [[dom/events/cut|'''oncut''']] event.

None.
To invoke this event, do one of the following:
*Right-click to display the shortcut menu and select Cut.
*Or press CTRL+X if the selection is within a text field.

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
*<code>[[dom/events/beforecopy|onbeforecopy]]</code>
*<code>[[dom/events/beforepaste|onbeforepaste]]</code>
*<code>oncopy</code>
*<code>[[dom/events/cut|oncut]]</code>
*<code>[[dom/events/paste|onpaste]]</code>
*<code>[[dom/methods/setData|setData]]</code>
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