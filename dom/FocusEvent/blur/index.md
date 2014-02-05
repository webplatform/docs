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
|Event_applies_to=dom/FocusEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/FocusEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to display the name of the object that has lost focus, that is, the object that fires the '''onblur''' event.
|Code=&lt;html&gt;
&lt;body&gt;
&lt;input type{{=}}"text" 
    name{{=}}"txtFName" 
    value{{=}}"First Name" 
    onblur{{=}}"console.log(event.srcElement.name)"&gt;
&lt;input type{{=}}"text" 
    name{{=}}"txtLName" 
    value{{=}}"Last Name" 
    onblur{{=}}"console.log(event.srcElement.name)"&gt;
&lt;input type{{=}}"text" 
    name{{=}}"txtPhone" 
    value{{=}}"Phone" 
    onblur{{=}}"console.log(event.srcElement.name)"&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onblurEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''onblur''' event fires on the original object before the [[dom/FocusEvent/focus|'''onfocus''']] or [[dom/HTMLElement/click|'''onclick''']] event fires on the object that is receiving focus. Where applicable, the '''onblur''' event fires after the [[dom/Element/change|'''onchange''']] event.
Use the focus events to determine when to prepare an object to receive or validate input from the user.
As of Microsoft Internet Explorer 5, you must set the [[html/attributes/tabIndex|'''tabIndex''']] attribute of elements that expose the '''onblur''' event.
For Internet Explorer 5 and later, the '''onblur''' event is asynchronous.
Switches focus away from the object on which the event is fired.
To invoke this event, do one of the following:
*Click the mouse on the document background or another control.
*Use the keyboard to navigate from one object to the next.
*Invoke the '''blur''' method when an object has focus.
*Switch focus to a different application or open a second window.

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
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


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