{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
For angle values in properties and their corresponding presentation attributes, the angle unit identifier is optional. If you do not  the identifier, the angle value is treated as if it is in degrees. If you provide the identifier, the angle unit identifier must be in lowercase.
When   you use angles  in an SVG attribute,  the '''angle''' property is defined as <code>deg</code> for degrees, <code>grad</code> for gradians, or <code>rad</code> for radians.
In the SVG DOM, '''angle''' values are represented by using [[svg/objects/SVGAngle|'''SVGAngle''']] or [[svg/objects/SVGAnimatedAngle|'''SVGAnimatedAngle''']] objects.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204732 Scalable Vector Graphics: Basic Data Types and Interfaces], Section 4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/objects/SVGPathSegArcAbs|SVGPathSegArcAbs]]</code>
*<code>[[svg/objects/SVGPathSegArcRel|SVGPathSegArcRel]]</code>
*<code>[[svg/objects/SVGTransform|SVGTransform]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}