{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Each document may have up to one active element.  Set the active element with the [[dom/HTMLElement/setActive|'''setActive''']] or [[dom/FocusEvent/focus|'''focus''']] methods.  Using the '''setActive''' method has no effect on document focus.  Using the '''focus''' method on an individual element causes the element to gain focus and become the active element, and this causes '''onfocusout''' to fire for this active element.
Using the [[dom/FocusEvent/focus|'''focus''']] method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus, and this causes '''onfocusout''' to fire for this active element.
For a given display, only one element has focus at any given time.  Striking a key directly affects only the element with focus.  Events fired by that keystroke may be scripted to affect other documents and child elements.
With Microsoft Internet Explorer 5.5 and later, focus on a [[dom/Document|'''Document''']] and the [[dom/Document/activeElement|'''active element''']] of a '''document''' can be managed separately.  Use the '''onfocusout''' event to manage formatting changes when an element loses focus.
To invoke this event, do one of the following:
*Click a [[dom/Document|'''Document''']], when the '''document''' does not have focus.
*Click an element, other than the current element with focus.
*Use the keyboard to move focus from the active element to another element.
*Invoke the [[dom/FocusEvent/focus|'''focus''']] method on an element, when the element is not the active element.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}