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
;''pEvt'' [in]:Type: '''<b>IDOMUIEvent'''</b>The [[dom/objects/Event|'''IDOMEvent''']] object.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/a|SVGAElement]]</code>
*<code>[[svg/elements/circle|SVGCircleElement]]</code>
*<code>[[svg/elements/clipPath|SVGClipPathElement]]</code>
*<code>[[svg/elements/defs|SVGDefsElement]]</code>
*<code>[[svg/elements/desc|SVGDescElement]]</code>
*<code>[[svg/elements/ellipse|SVGEllipseElement]]</code>
*<code>[[svg/elements/g|SVGGElement]]</code>
*<code>[[svg/elements/gradient|SVGGradientElement]]</code>
*<code>[[svg/elements/image|SVGImageElement]]</code>
*<code>[[svg/elements/line|SVGLineElement]]</code>
*<code>[[svg/elements/marker|SVGMarkerElement]]</code>
*<code>[[svg/elements/mask|SVGMaskElement]]</code>
*<code>[[svg/elements/metadata|SVGMetadataElement]]</code>
*<code>[[svg/elements/path|SVGPathElement]]</code>
*<code>[[svg/elements/patterrn|SVGPatternElement]]</code>
*<code>[[svg/elements/polygon|SVGPolygonElement]]</code>
*<code>[[svg/elements/polyline|SVGPolylineElement]]</code>
*<code>[[svg/elements/rect|SVGRectElement]]</code>
*<code>[[svg/elements/script|SVGScriptElement]]</code>
*<code>[[svg/elements/stop|SVGStopElement]]</code>
*<code>[[svg/elements/style|SVGStyleElement]]</code>
*<code>[[svg/elements/svg|SVGSVGElement]]</code>
*<code>[[svg/elements/switch|SVGSwitchElement]]</code>
*<code>[[svg/elements/symbol|SVGSymbolElement]]</code>
*<code>[[svg/elements/text|SVGTextElement]]</code>
*<code>[[svg/elements/tspan|SVGTSpanElement]]</code>
*<code>[[svg/elements/textPath|SVGTextPathElement]]</code>
*<code>[[svg/elements/use|SVGUseElement]]</code>
*<code>[[svg/elements/view|SVGViewElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}