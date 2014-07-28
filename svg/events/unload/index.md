{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
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
|Interface=dom/objects/Event
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

The '''onunload''' event occurs when the DOM implementation removes a document from a window or frame. This event  applies  only  to  the outermost [[svg/elements/svg|'''svg''']] element.

The object or document  is removed from the browser window.
To invoke this event, do one of the following:
*The DOM implementation removes a document from a window or frame.
|Import_Notes====Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204745 Scalable Vector Graphics: Scripting], Section 18.4.3

===Event handler parameters===

;''pEvt'' [in]:Type: '''IDOMUIEvent'''The [[dom/objects/Event|'''IDOMEvent''']] object.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===

*[[svg/elements/svg|'''SVGSVGElement''']]
*[[dom/events/unload|'''onunload''']]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}