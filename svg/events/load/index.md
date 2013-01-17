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

The '''onload'''  event  occurs  when the browser has fully parsed the element and its descendants and is ready to act appropriately on that element, such as rendering  the element to the target device. Before the event occurs, the browser must have loaded, parsed, and prepared referenced external resources  for  rendering. Optional external resources are not required to be ready for the event to occur.

The object  that  the event is specified for is loaded.
To invoke this event, do one of the following:
*A user opens a page in the browser to  fire  this event for the document or any object within it.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204745 Scalable Vector Graphics: Scripting], Section 18.4.2

===Event handler parameters===

;''pEvt'' [in]:Type: '''IDOMUIEvent'''The [[dom/objects/Event|'''IDOMEvent''']] object.

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/a|'''SVGAElement''']]
*[[svg/elements/circle|'''SVGCircleElement''']]
*[[svg/elements/clipPath|'''SVGClipPathElement''']]
*[[svg/elements/defs|'''SVGDefsElement''']]
*[[svg/elements/desc|'''SVGDescElement''']]
*[[svg/elements/ellipse|'''SVGEllipseElement''']]
*[[svg/elements/g|'''SVGGElement''']]
*[[svg/elements/gradient|'''SVGGradientElement''']]
*[[svg/elements/image|'''SVGImageElement''']]
*[[svg/elements/line|'''SVGLineElement''']]
*[[svg/elements/marker|'''SVGMarkerElement''']]
*[[svg/elements/mask|'''SVGMaskElement''']]
*[[svg/elements/metadata|'''SVGMetadataElement''']]
*[[svg/elements/path|'''SVGPathElement''']]
*[[svg/elements/patterrn|'''SVGPatternElement''']]
*[[svg/elements/polygon|'''SVGPolygonElement''']]
*[[svg/elements/polyline|'''SVGPolylineElement''']]
*[[svg/elements/rect|'''SVGRectElement''']]
*[[svg/elements/script|'''SVGScriptElement''']]
*[[svg/elements/stop|'''SVGStopElement''']]
*[[svg/elements/style|'''SVGStyleElement''']]
*[[svg/elements/svg|'''SVGSVGElement''']]
*[[svg/elements/switch|'''SVGSwitchElement''']]
*[[svg/elements/symbol|'''SVGSymbolElement''']]
*[[svg/elements/text|'''SVGTextElement''']]
*[[svg/elements/tspan|'''SVGTSpanElement''']]
*[[svg/elements/textPath|'''SVGTextPathElement''']]
*[[svg/elements/use|'''SVGUseElement''']]
*[[svg/elements/view|'''SVGViewElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}