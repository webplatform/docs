{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the [[dom/DataTransfer/setData|'''setData''']] and [[dom/DataTransfer/getData|'''getData''']] methods with the [[dom/ClipboardData|'''ClipboardData''']] object to perform a cut-and-paste operation through the shortcut menu.
|Code=&lt;head&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Creating custom code for cutting requires several steps:
#Set '''event.returnValue{{=}}false''' in the '''onbeforecut''' event to enable the Cut shortcut menu item.
#Specify a data format in which to transfer the selection through the [[dom/DataTransfer/setData|'''setData''']] method.
#Invoke the [[dom/DataTransfer/setData|'''setData''']] method in the [[dom/Event/cut|'''oncut''']] event.

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
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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