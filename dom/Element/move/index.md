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
|Description=The following example shows how to use the '''onmove''' event and display the x and y coordinates of a '''DIV''' as it is moved.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;title&gt;The onmove event&lt;/title&gt;
&lt;script&gt;
// Turn on 2-D positioning
document.execCommand("2D-position",false,true);
function fnHandleMove() {
  oXDelta.innerText {{=}} event.srcElement.offsetLeft;
  oYDelta.innerText {{=}} event.srcElement.offsetTop; 
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body onmove{{=}}"fnHandleMove();"&gt;
&lt;b&gt;Current Object:&lt;/b&gt;&lt;br&gt;
X delta: &lt;span id{{=}}"oXDelta"&gt;n/a&lt;/span&gt;&lt;br&gt;
Y delta: &lt;span id{{=}}"oYDelta"&gt;n/a&lt;/span&gt;&lt;br&gt;
&lt;div contenteditable{{=}}"true"&gt;
&lt;div style{{=}}"width:300px;height:100px; background-color:red; position:absolute;"&gt;
Movable DIV&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmoveEx1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This event can be bound to relatively positioned elements as well as absolutely positioned elements.
This event does not fire when it is bound to an object inside a container object that moves.
Calls the associated event handler if there is one.
To invoke this event, do one of the following:
*Change the absolute position of the object.

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