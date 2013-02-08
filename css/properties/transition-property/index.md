{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The 'transition-property' property specifies the name of the CSS property to which the transition is applied.}}
{{CSS Property
|Initial value=all
|Applies to=all elements, :before and :after pseudo elements
|Inherited=No
|Media=visual
|Animatable=Yes
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=No transition effect is applied (all transition properties are ignored) when a new property value is specified.
}}{{CSS Property Value
|Data Type=all
|Description=All properties that support transitions have the transition effect applied when a new value for the property is specified. (Default)
}}{{CSS Property Value
|Data Type=propertyname
|Description=A list of properties, separated by commas, to which the transition effect is applied.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The version of this property using a vendor prefix, '''-ms-transition-property''', has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/css3-transitions/#transition-property-property CSS Transitions Module Level 3], Section 2.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=22.0
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=5.1
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transistions
|Manual_sections=

}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}