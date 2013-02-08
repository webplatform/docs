{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=0
|Applies to=all elements, :before and :after pseudo elements
|Inherited=No
|Media=interactive
|Animatable=No
|Values={{CSS Property Value
|Data Type=time
|Description=Floating-point number, followed by a time units designator (<code>ms</code> or <code>s</code>). For more information about the supported time units, see '''CSS Values and Units Reference'''.

This property accepts <code>s</code> and <code>ms</code> as valid units of time.
Values are rounded up to the second decimal place.
Each '''transition-delay''' is paired with a corresponding object property  identified in the [[css/properties/transition-property|'''transition-property''']] property.
If more '''transition-delay''' values are declared than corresponding object properties identified in the [[css/properties/transition-property|'''transition-property''']] property, the excess '''transition-delay''' values are ignored.
If fewer  '''transition-delay''' values are declared than corresponding object properties identified in the [[css/properties/transition-property|'''transition-property''']] property, the list of '''transition-delay''' values is repeated from the beginning until the object properties are exhausted.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 2.4
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
|Chrome_prefixed_version=22
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}