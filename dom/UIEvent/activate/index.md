{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Fires when the object is set as the active element.}}
{{Event
|Event_applies_to=dom/UIEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=No
|Default_action=see Notes
|Interface=dom/UIEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example demonstrates the order of event firing for the '''onactivate''' and '''onload''' events. As each event fires, it appends a string to the '''div''' element within the document. The '''onactivate''' event fires before the '''onload''' event.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function fnActivate(){
    oDIV1.innerHTML +{{=}} "&lt;br/&gt;&lt;br/&gt;The &lt;b&gt;onactivate&lt;/b&gt; event, available as of 
        Internet Explorer 5.5, fires first on the body element.";
}
function fnLoad(){
    oDIV1.innerHTML +{{=}} "&lt;br/&gt;&lt;br/&gt;The &lt;b&gt;onload&lt;/b&gt; event, available as of  
        Internet Explorer 4.0, fires after the &lt;i&gt;onactivate&lt;/i&gt; event fires 
        on the body element.";
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body onactivate{{=}}"fnActivate();" onload{{=}}"fnLoad();"&gt; 
&lt;div id{{=}}"oDIV1"&gt;&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onactivate.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  Using the [[dom/HTMLElement/setActive|'''setActive''']] method has no effect on document focus.  Using the [[dom/HTMLElement/focus|'''focus''']] method on an individual element causes the element to gain focus and become the active element.
When one object loses activation and another object becomes the [[dom/Document/activeElement|'''activeElement''']], the '''onfocus''' event fires on the object becoming the '''activeElement''' only after the [[dom/HTMLElement/blur|'''onblur''']] event fires on the object losing activation.
Each document may have up to one active element.  Set the active element with the '''setActive''' or '''focus''' methods.
Using the '''focus''' method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus.
The '''onactivate''' event fires before the '''onload''' event for any of the objects listed in the Applies To section.
For Microsoft Internet Explorer 6 and later, the '''event.fromElement''' property is now exposed by this event.
For Microsoft Internet Explorer 5.5 and later, focus on a [[dom/Document|'''Document''']], and the '''activeElement''' of a '''Document''' can be managed separately.  Use the '''onactivate''' event to manage formatting changes when an element is made active.
Change activation from the '''event.fromElement''' to the '''event.srcElement'''.
To invoke this event, do one of the following:
*Click an element other than the '''activeElement''' element of the document.
*Use the keyboard to move focus from the active element to another element.
*Invoke the '''setActive''' method on an element, when the element is not the active element.

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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536787(v=vs.85).aspx active Event]
|HTML5Rocks_link=
}}