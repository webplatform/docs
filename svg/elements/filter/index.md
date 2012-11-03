{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Needed, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|SVG filter effects apply graphics operations such as blurs and color transformations to a source graphic. Filters may be applied to any SVG element. The <code>filter</code> element specifies the position, dimensions, resolution and units for a filter effect. <code>filter</code>elements typically have multiple child elements that declare a graph of filter primitives such as feGaussianBlur or feColorMatrix, which create the graphics effects.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
|Content=The Filte
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
A filter element is never rendered directly. It is only referenced using the filter property on the element to which the filter is applied. Note that the [[css/properties/display|'''display''']] property does not apply to the <code>filter</code> element and  elements are not directly rendered even if the '''display''' property is set to a value other than "none".   Conversely, <code>filter</code> elements are available for referencing even when the'''display''' property on the <code>filter</code>element or any of its ancestors is set to "none".
|Import_Notes====Syntax===
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
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=SVG 1.1 (Second Edition)
|URL=www.w3.org/TR/SVG/
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=<filter>
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=<filter>
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=RIM OS2
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=IE10 
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=iOS 6
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}