{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when the user moves the mouse pointer outside the boundaries of the object.}}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Default_action=none
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the difference between mouseout and mouseleave events.
|Code=var el = document.getElementById("test");
  function domouseleave(evt){
  if(!evt)evt=window.event;
  var el=(evt.target)?evt.target:evt.srcElement;
  el.style.color='purple';
  setTimeout(function(){
  	el.style.color='';
  	},500);
  }
  function domouseout(evt){
  if(!evt)evt=window.event;
  var el=(evt.target)?evt.target:evt.srcElement;
  el.style.color='orange';
  setTimeout(function(){
  	el.style.color='';
  	},500);
  }
  if(el.addEventListener){
  	el.addEventListener('mouseleave',domouseleave,false);
  	el.addEventListener('mouseout',domouseout,false);
  }
  else{
  	el.attachEvent('onmouseleave',domouseleave);
  	el.attachEvent('onmouseout', domouseout);
  }
|LiveURL=http://result.dabblet.com/gist/eaba649bc760d5831769/40c8a5bde01f6ac7896353103b65313d550aed40
}}
}}
{{Notes_Section
|Usage=Could be used, for example to play a sound as the user hovers over a menu list.
|Notes====Remarks===
The event fires only if the mouse pointer is inside the boundaries of the object and the user moves the mouse pointer outside the boundaries of the object. If the mouse pointer is  currently outside the boundaries of the object, for the event to fire, the user must move the mouse pointer inside the boundaries of the object and then back outside the boundaries of the object.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse pointer outside the boundaries of an object.

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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/Events/mouseleave mouseleave event]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536946(v=vs.85).aspx mouseleave event]
|HTML5Rocks_link=
}}