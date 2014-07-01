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
|Description=The following example shows how to use the '''onmoveend''' event with a movable '''DIV''' and have the background color and inner text change when the mouse button is released and the '''DIV''' stops moving.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;Editing events sample page&lt;/TITLE&gt;
&lt;SCRIPT&gt;
// Turn on 2D positioning
document.execCommand("2D-position",false,true);
// Fires when the onmovestart event is fired
function fnHandleMoveStart() {
  var oDiv {{=}} event.srcElement
  oDiv.style.backgroundColor {{=}} "green";
  oDiv.innerText {{=}} "I Started Moving";
}
// Function called when the onmoveend event is fired
function fnHandleMoveEnd() {
  var oDiv {{=}} event.srcElement
  oDiv.style.backgroundColor {{=}} "red";
  oDiv.innerText {{=}} "I Stopped";
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onmovestart{{=}}"fnHandleMoveStart();" onmoveend{{=}}"fnHandleMoveEnd();"&gt;
&lt;DIV CONTENTEDITABLE{{=}}"true"&gt;
&lt;DIV style{{=}}"width:300px;height:100px; color:white; background-color:red; 
position:absolute;"&gt;
My DIV&lt;/DIV&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmovestartendEx1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''onmoveend''' event fires only when an editable element stops moving.
This event can only be bound to absolutely positioned elements.
Calls the associated event handler if there is one.
To invoke this event, do one of the following:
*Stop moving the editable object.

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