{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

Returns a [[dom/properties/controlRange|'''controlRange''']] collection if sucessful or a null value otherwise.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example creates a [[dom/properties/controlRange|'''controlRange''']] by using the '''createControlRange''' method.
|LiveURL=
|Code=
oControlRange {{=}} document.body.createControlRange();
}}}}
{{Notes_Section
|Notes=
===Remarks===
Creates a selection range object for control-based selection rather than text-based selection.
If a [[dom/properties/controlRange|'''controlRange''']] already exists, '''createControlRange''' overwrites the existing element; otherwise, it returns a pointer to the element created.
If there are currently controls selected in the text container, the control range is initialized with them; otherwise, it is created empty and controls need to be explicitly added to it. This is opposite of the text range, which defaults to the whole text container if there is no selection.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>body</code>
*<code>[[dom/traversal/methods/createRange (selection)|createRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}