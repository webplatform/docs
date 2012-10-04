{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
A filter element is never rendered directly. It is only referenced using the a filter property on the element to which the filter is applied. Note that the [[css/properties/display|'''display''']] property does not apply to the <code>filter</code> element and  elements are not directly rendered even if the '''display''' property is set to a value other than "none".   Conversely, <code>filter</code> elements are available for referencing even when the'''display''' property on the <code>filter</code>element or any of its ancestors is set to "none".
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.1


===Members===
The '''SVGFilterElement''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''SVGFilterElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/setFilterRes|'''setFilterRes''']]
|Sets the X and Y values of the [[svg/properties/filterResX|'''filterRes''']] attribute.
|}
 

====Properties====
The '''SVGFilterElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/className|'''className''']]
|Gets  the names of the classes  that are assigned to this object.
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/properties/filter|'''filter''']]
|The [[svg/properties/filter|'''filter''']] property is generally used to apply a previously define '''filter''' to an applicable element.
|-
|[[svg/properties/filterResX|'''filterResX''']]
|Corresponds to the X component of the attribute filterRes on the given filter element.
|-
|[[svg/properties/filterResY|'''filterResY''']]
|Corresponds to the Y component of the attribute filterRes on the given filter element.
|-
|[[svg/properties/filterUnits|'''filterUnits''']]
|Defines the coordinate system for the filter attributes.
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/properties/primitiveUnits|'''primitiveUnits''']]
|Specifies the coordinate system for the various length values within the filter primitives and for the attributes that define the filter primitive subregion. The filter primitives identify a subregion which restricts calculation and rendering of the given filter primitive. The default filter primitive subregion is equal to the filter region.
|-
|[[svg/properties/style|'''style''']]
|Gets a [[css/cssom/style|'''style''']] object.
|-
|[[svg/properties/width|'''width''']]
|Defines the width of an element.
|-
|[[svg/properties/x|'''x''']]
|Gets or sets the x-coordinate value.
|-
|[[svg/properties/xmllang|'''xmllang''']]
|Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
|-
|[[svg/properties/xmlspace|'''xmlspace''']]
|Gets or sets a value that indicates whether white space is preserved in character data.
|-
|[[svg/properties/y|'''y''']]
|Gets or sets the y-coordinate value.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}