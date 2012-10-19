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
{{Topics|Events}}
{{Notes_Section
|Notes=
===Remarks===
The  '''onresize''' event applies only  to the outermost [[svg/elements/svg|'''svg''']] element and is dispatched after the resize operation finishes.
N/A
To invoke this event, do one of the following:
*The user changes the size of the document view.

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
*<code>[[dom/events/resize|onresize]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}