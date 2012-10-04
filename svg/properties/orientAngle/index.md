{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
If the [[svg/properties/orientType|'''orientType''']] property  is <code>SVG_MARKER_ORIENT_ANGLE</code>, this  property represents the angle value for '''orientAngle'''; otherwise, this property is set to zero.
|Import_Notes=
===Syntax===
HRESULT value {{=}} object.put_orientAngle(ISVGAnimatedAngle* v);HRESULT value {{=}} object.get_orientAngle(ISVGAnimatedAngle** p);
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199816 Scalable Vector Graphics: Painting, Filling, Stroking and Marker Symbols], Section 11.9.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>[[svg/elements/marker|SVGMarkerElement]]</code>
*<code>SVGMarkerElement</code>
*<code>[[svg/properties/orientType|orientType]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}