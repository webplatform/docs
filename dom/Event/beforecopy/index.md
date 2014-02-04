{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
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
|Description=This example uses the '''onbeforecopy''' event to customize copy behavior.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
var sNewValue {{=}} "copy event fired";
var bFired {{=}} false;
var sSave {{=}} "";
function Source_Beforecopy() 
{
  sSave {{=}} oSource.innerText;
  bFired {{=}} true;
  event.returnValue {{=}} false;
}
function Source_Copy() 
{
  window.clipboardData.setData("Text", sNewValue);
}
function Target_BeforePaste() 
{
  event.returnValue {{=}} false;
}
function Target_Paste() 
{
  event.returnValue {{=}} false;
  oTarget.value {{=}} window.clipboardData.getData("Text");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;SPAN ID{{=}}oSource onbeforecopy{{=}}"Source_Beforecopy()"
       oncopy{{=}}"Source_Copy()"&gt;copy this text&lt;/SPAN&gt;
&lt;INPUT ID{{=}}oTarget onbeforepaste{{=}}"Target_BeforePaste()"
       onpaste{{=}}"Target_Paste()"&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecopyEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''onbeforecopy''' event fires on the source element. Use the [[dom/DataTransfer/setData|'''setData''']] method to specify a data format for the selection.
None.
To invoke this event, do one of the following:
*Right-click to display the shortcut menu and select Copy.
*Or press CTRL+C.

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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}