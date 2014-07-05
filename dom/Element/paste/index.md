{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec, and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the [[dom/ClipboardData|'''ClipboardData''']] object to implement custom editing functionality.
|Code=&lt;HEAD&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Creating custom code to enable the Paste command requires several steps.
#Set the event object [[dom/BeforeUnloadEvent/returnValue|'''returnValue''']] to false in the [[dom/Event/beforepaste|'''onbeforepaste''']] event to enable the Paste shortcut menu item.
#Cancel the default behavior of the client by setting the event object '''returnValue''' to false in the '''onpaste''' event handler. This applies only to objects, such as the '''text box''', that have a default behavior defined for them.
#Specify a data format in which to paste the selection through the [[dom/DataTransfer/getData|'''getData''']] method.
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