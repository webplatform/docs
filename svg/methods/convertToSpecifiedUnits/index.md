{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
The '''convertToSpecifiedUnits''' method preserves the same underlying stored value, but it resets the stored unit identifier to the  specified  ''unitType'' type. The [[svg/properties/unitType  (SVGLength)|'''unitType''']], [[svg/properties/valueInSpecifiedUnits|'''valueInSpecifiedUnits''']], and [[svg/properties/valueAsString|'''valueAsString''']]  objects might be modified  when you call  this method.
|Import_Notes=
===Syntax===
<div class{{=}}"code">HRESULT retVal {{=}} ''object.''convertToSpecifiedUnits(unitType);</div>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204732 Scalable Vector Graphics: Basic Data Types and Interfaces], Section 4.5.11


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/objects/SVGAngle|SVGAngle]]</code>
*<code>[[svg/objects/SVGLength|SVGLength]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}


[[Category:SVG]]