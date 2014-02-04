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
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  When focus leaves the document, the active element does not change and the '''onbeforedeactivate''' event will not fire.
Each document may have up to one active element.  Set the active element with the [[dom/HTMLElement/setActive|'''setActive''']] or [[dom/HTMLElement/focus|'''focus''']] methods.  Using the '''setActive''' method has no effect on document focus.  Using the '''focus''' method on an individual element causes the element to gain focus and become the active element.
Using the '''focus''' method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus.
For a given display, only one element has focus at any given time.  Striking a key directly affects only the element with focus.  Events fired by that keystroke may be scripted to affect other documents and child elements.
With Microsoft Internet Explorer 5.5 and later, focus on a [[dom/Document|'''Document''']], and the [[dom/Document/activeElement|'''active element''']] of a '''document''' can be managed separately.  Use the '''onbeforedeactivate''' event to cancel moving activation from the current element.
Change activation from the '''event'''.'''srcElement''' to the '''event'''.'''toElement'''.
To invoke this event, do one of the following:
*Click an element, other than the [[dom/properties/activeElement|'''active''']] element of the document.
*Use the keyboard to move focus from the active element to another element.
*Invoke the [[dom/HTMLElement/setActive|'''setActive''']] method on an element, when the element is not the active element.
*Invoke the [[dom/HTMLElement/focus|'''focus''']] method on an element, when the element is not the active element.

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