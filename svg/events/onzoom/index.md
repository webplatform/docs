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

The '''onzoom''' event occurs when the zoom level of a document view is  changed  through a direct user interaction or any change to the [[svg/properties/currentScale|'''currentScale''']]  property that is available on the [[svg/elements/svg|'''svg''']] element. This event  applies only  to the outermost '''svg''' element and is dispatched after the zoom-level modification  occurs.

Changes the document's zoom level  or [[svg/properties/currentScale|'''currentScale''']] property.
To invoke this event, do one of the following:
*The user changes the zoom level of the document or the value of the [[svg/elements/svg|'''svg''']] element's [[svg/properties/currentScale|'''currentScale''']] property.
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
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}