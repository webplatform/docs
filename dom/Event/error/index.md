{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when an error occurs.}}
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
|Language=JavaScript
|Description=The following examples use the '''onerror''' event to handle run-time script errors and object load errors.

The following example specifies an invalid script entry. The script in the text field is evaluated when the Throw Error button is clicked. The '''onerror''' event fires because the script is invalid. The error results are inserted at the bottom of the sample page instead of in a dialog box.
|Code=&lt;script&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX.htm
}}{{Single Example
|Language=JavaScript
|Description=The following example shows how to set the handler for the '''onerror''' event in script before an image source is specified. When the invalid source is set on the '''img''' element, the event fires.
|Code=&lt;script&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onerrorEX1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
To suppress the default Windows Internet Explorer error message for the '''window''' event, set the [[dom/BeforeUnloadEvent/returnValue|'''returnValue''']] property to '''true''' or simply return <code>true</code> in Microsoft JScript.
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