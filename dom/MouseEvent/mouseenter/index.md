{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when the user moves the mouse pointer into the object.}}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=Yes
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The event handler bigImg() is triggered when the user moves the mouse pointer over the image.
The event handler normalImg() is triggered when the mouse pointer is moved out of the image.
|Code=function bigImg(evt){
if(!evt)evt=window.event;
var el=(evt.target)?evt.target:evt.srcElement;
el.style.height="64px";
el.style.width="64px";
}
function normalImg(evt){
if(!evt)evt=window.event;
var el=(evt.target)?evt.target:evt.srcElement;
el.style.height="32px";el.style.width="32px";
}
if(window.addEventListener){
document.getElementById('imgSmiley').addEventListener('mouseover',bigImg,false);
document.getElementById('imgSmiley').addEventListener('mouseout',normalImg,false);
}
else{
document.getElementById('imgSmiley').attachEvent('onmouseover',bigImg);
document.getElementById('imgSmiley').attachEvent('onmouseout',normalImg);
}
|LiveURL=http://result.dabblet.com/gist/acdd7a0b0ebdfaf3699d/a7e519705e7c6bf677b92d98ceaeb513ff37425a
}}{{Single Example
|Language=HTML
|Description=MSDN Example using the mouseover event attribute.
|Code=&lt;p&gt;
	onmouseover{{=}}"this.style.color='red'" 
    onmouseout{{=}}"this.style.color='black'"&gt;
    	Move the mouse pointer over this text to change its color. Move the pointer off the text 
        to change the color back.
&lt;/p&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm
}}
}}
{{Notes_Section
|Usage=Use to perform an action when the mouse cursor is moved over an element. 
Alternatively, for CSS2 compliant userAgents use the :hover pseudo class.
|Notes====Remarks===
The event fires only if the mouse pointer is outside the boundaries of the object and the user moves the mouse pointer inside the boundaries of the object. If the mouse pointer is currently inside the boundaries of the object, for the event to fire, the user must move the mouse pointer outside the boundaries of the object and then back inside the boundaries of the object.
Unlike the [[dom/MouseEvent/mouseover|'''onmouseover''']] event, the '''onmouseenter''' event does not bubble.  In other words, the '''onmouseenter''' event does not fire when the user moves the mouse pointer over elements contained by the object, whereas '''onmouseover''' does fire.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse pointer inside the boundaries of an object.

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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/Events/mouseover mouseover event]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536949(v=vs.85).aspx mouseover event]
|HTML5Rocks_link=
}}