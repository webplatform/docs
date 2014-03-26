{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Selection
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

Returns a collection of [[dom/TextRange|'''TextRange''']] objects.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Host applications can provide a multiple selection mechanism and can return a collection
of [[dom/TextRange|'''TextRange''']] objects that represents discontinuous selections.
The host application provides the collection through the '''ISegmentList'''
interface. ''MSHTML'' requests this interface through the '''ISelectionServices''' interface.
Microsoft Internet Explorer 5.5 does not provide multiple selection. The default implementation of this
method returns a collection consisting of a single [[dom/TextRange|'''TextRange''']] object.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}