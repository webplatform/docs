{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Fires when the user aborts the download.}}
{{Event
|Event_applies_to=dom/UIEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=Yes
|Default_action=Halts downloading of the designated image, but not due to an error
|Interface=dom/UIEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=&lt;img id{{=}}"imgLogo" title{{=}}"Click to view larger image" src{{=}}"example.com/small.jpg" alt{{=}}"small logo"/&gt;
&lt;script type{{=}}"text/javascript"&gt;
var myAddEvent=function(el, ev, fn){
	if(el.addEventListener){
		el.addEventListener(ev, fn, false);
	}else if(el.attachEvent){
		el.attachEvent('on'+ev,fn);
	}else{
		el['on'+ ev] = fn;
	}
};
var el{{=}}document.getElementById('imgLogo');
function imgAbortHandler(evt){
// code to recover from the abort method.
}
function imgResize(evt){
document.getElementById('imgLogo').src{{=}}'http://example.com/big.jpj';
document.getElementById('imgLogo').title{{=}}'big logo';
}
myAddEvent(el,'click',imgResize);
myAddEvent(el,'abort',imgAbortHandler);
}}
}}
{{Notes_Section
|Usage=Used to recover the original resource if the user cancels the download.
|Notes====Remarks===
Halts downloading of the designated image, but not due to an error.
To invoke this event, do one of the following:
*Click an [[html/elements/a|'''anchor''']] while the document is loading.
*Stop loading the document.
*Navigate to another document.
*Windows Internet Explorer 9. The client stops fetching media data, but not due to an error.

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
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 6.1.6.2


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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/Events/abort abort]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536785(v=vs.85).aspx abort Event]
|HTML5Rocks_link=
}}