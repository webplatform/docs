{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets all the top border properties in one declaration.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS object model property=borderTop
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<border-width> <border-style> <color>
|Description=Any of the range of width values available to the [[css/properties/border-top-width|'''border-top-width''']] property.
The <tt>border-top</tt> property is a shorthand property for setting the same width, color, and style for top border of a box.
* Width - Any of the range of width values available to the [[css/properties/border-width|'''border-width''']] property. Default value is <tt>medium</tt>.
* Style - Any of the range of style values available to the [[css/properties/border-style|'''border-style''']] property. Default value is <tt>none</tt>.
* Color - Any of the range of color values available to the [[css/properties/border-color|'''border-color''']] property. Default value is the value of the element's [[css/properties/color|'''color''']] property - i.e. text color.
}}{{CSS Property Value
|Data Type=inherit
|Description=When we set the value to <tt>inherit</tt>, the element will use border values set on its parent
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''border-top''' property is a composite property that sets the '''width''', '''color''', and '''style''' values for the top border of an object.
All individual border properties not set by the composite '''border-top''' property are set to their default values. For example, the default value for '''width''' is '''medium'''.
If a '''color''' is not specified, the text color is used.
For more information about supported colors, see the Color Table.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms530739(v=vs.85).aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}