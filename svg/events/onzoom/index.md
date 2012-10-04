{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Event}}
{{Notes_Section
|Notes=
===Remarks===
The '''onzoom''' event occurs when the zoom level of a document view is  changed  through a direct user interaction or any change to the [[svg/properties/currentScale|'''currentScale''']]  property that is available on the [[svg/elements/svg|'''svg''']] element. This event  applies only  to the outermost '''svg''' element and is dispatched after the zoom-level modification  occurs.
Changes the document's zoom level  or [[svg/properties/currentScale|'''currentScale''']] property.
To invoke this event, do one of the following:
*The user changes the zoom level of the document or the value of the [[svg/elements/svg|'''svg''']] element's [[svg/properties/currentScale|'''currentScale''']] property.

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204745 Scalable Vector Graphics: Scripting], Section 18.4.3


===Event handler parameters===
;''pEvt'' [in]:Type: '''<b>IDOMUIEvent'''</b>The [[dom/objects/Event|'''IDOMEvent''']] object.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/svg|SVGSVGElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}