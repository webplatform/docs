{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
The '''cx''' property defines the x-coordinate for the center of the largest (that is, outermost) circle of a radial gradient. The gradient is drawn such that the 100% gradient [[svg/elements/stop|'''stop''']] is mapped to the perimeter of this largest (that is, outermost) circle. If you do not specify the '''cx''' property, the effect is the same as if you specify a value of <code>50%</code>.
The '''cx''' value can be a percentage. When [[svg/properties/gradientUnits|'''gradientUnits''']] is  '''userSpaceOnUse''', percentages represent values that are relative to the current viewport. When '''gradientUnits''' is  '''objectBoundingBox''', percentages represent values that are relative to the bounding box for the object.
Properties inherit into the [[svg/elements/radialGradient|'''radialGradient''']] element from its ancestors. Properties do not inherit from the element that references the '''radialGradient''' element.
[[svg/elements/radialGradient|'''radialGradient''']] elements are never rendered directly. They exist so that you can reference  them by using the <code>fill</code> and <code>stroke</code> properties.
The <code>display</code> property does not apply to the [[svg/elements/radialGradient|'''radialGradient''']] element  so '''radialGradient''' elements are not directly rendered even if the <code>display</code> property is set to a value other than <code>none</code>.  '''radialGradient''' elements are available for referencing even when the <code>display</code> property on the '''radialGradient''' element or any of its ancestors is set to <code>none</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/radialGradient|SVGRadialGradientElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}