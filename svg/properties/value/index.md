{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

For angles,  the '''value'''  property is in degrees. For lengths, the '''value'''  property is in user units.
If you

set the '''value''' property, the  [[svg/properties/valueInSpecifiedUnits|'''valueInSpecifiedUnits''']] and [[svg/properties/valueAsString|'''valueAsString''']]  properties are updated automatically to reflect this setting.
|Import_Notes=

===Syntax===

HRESULT value {{=}} object.put_value(float v);HRESULT value {{=}} object.get_value(float* p);

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204732 Scalable Vector Graphics: Basic Data Types and Interfaces], Section 4.5.11

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/objects/SVGAngle|'''SVGAngle''']]
*[[svg/objects/SVGLength|'''SVGLength''']]
*[[svg/objects/SVGNumber|'''SVGNumber''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]