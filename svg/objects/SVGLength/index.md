{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=

===Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

You can designate an '''SVGLength''' object as read-only, so that attempts to modify the object raises  an '''NoModificationAllowedError''' exception.

|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204732 Scalable Vector Graphics: Basic Data Types and Interfaces], Section 4.5.11

===Members===

The '''SVGLength''' object has these methods:

*[[svg/methods/convertToSpecifiedUnits|'''convertToSpecifiedUnits''']]: Changes the stored unit identifier to the specified type.
*[[svg/methods/newValueSpecifiedUnits|'''newValueSpecifiedUnits''']]: Resets the  specified  value as a number with the specified '''unit type''',  replacing the values for all of the attributes on the object.

The '''SVGLength''' object has these properties:

*[[svg/properties/unitType  (SVGLength)|'''unitType''']]: Gets or sets a value that indicates the type of length units.
*[[svg/properties/value|'''value''']]: Gets or sets the value of the given attribute.
*[[svg/properties/valueAsString|'''valueAsString''']]: Gets or sets the string form of the [[svg/properties/value|'''value''']] property, in the units that '''svgUnitTypes''' specifies.
*[[svg/properties/valueInSpecifiedUnits|'''valueInSpecifiedUnits''']]: Gets or sets the length or angle value, as a floating point number, in the units that '''svgUnitTypes''' specifies.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}