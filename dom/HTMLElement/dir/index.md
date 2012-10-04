{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Unless explicitly set, the '''dir''' property has no return value when accessed in script.
The '''dir''' property does not affect alphanumeric characters in Latin documents. These characters always render '''ltr'''.  However, the property does affect punctuation characters in Latin documents. For example, punctuation marks such as periods and question marks will render to the left of a sentence when the '''dir''' property is set to '''rtl'''.
The value of '''dir''' property has no effect on the orientation of coordinates for an object's positioning properties. For example, the  [[css/properties/left|'''left''']] property and the [[css/properties/right|'''right''']] property perform the same placement in both cases.  However, when both the '''left''' and '''right''' properties are specified, the '''left''' property takes precedence when the '''dir''' property is set to '''ltr'''. Likewise, the '''right''' property takes precedence when the '''dir''' property is set to '''rtl'''.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Reference</code>
*<code>[[css/properties/direction|direction]]</code>
*<code>Conceptual</code>
*<code>HTML Character Sets</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}