{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Selection
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

Returns a collection of [[dom/traversal/TextRange|'''TextRange''']] objects.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
Host applications can provide a multiple selection mechanism and can return a collection
of [[dom/traversal/TextRange|'''TextRange''']] objects that represents discontinuous selections.
The host application provides the collection through the '''ISegmentList'''
interface. ''MSHTML'' requests this interface through the '''ISelectionServices''' interface.
Microsoft Internet Explorer 5.5 does not provide multiple selection. The default implementation of this
method returns a collection consisting of a single [[dom/traversal/TextRange|'''TextRange''']] object.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/selection|selection]]</code>
*<code><b/></code>
*<code>ISelectionServices</code>
*<code>ISegmentList</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}