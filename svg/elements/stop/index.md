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
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

You must define two '''stop''' elements  to  create  a gradient effect. If no  '''stop''' elements,  painting occurs as if you specify '''none'''  as the paint style. If you define one '''stop'''  element,  the paint  occurs by using a solid-color fill  with  the color that is defined for that gradient '''stop''' element.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.4

===Members===

The '''SVGStopElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGStopElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/offset|'''offset''']]: Gets or sets  a value that indicates where the gradient stop is placed within the gradient.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/attributes/stop-color|'''stopColor''']]: Sets or retrieves a value that indicates what color to use at the current gradient stop.
*[[svg/attributes/stop-opacity|'''stopOpacity''']]: Sets or retrieves a value that defines the opacity of the current gradient stop.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
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

===Reference===

*[[svg/elements/linearGradient|'''SVGLinearGradientElement''']]
*[[svg/elements/radialGradient|'''SVGRadialGradientElement''']]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}