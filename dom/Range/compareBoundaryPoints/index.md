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
|Parameters={{Method Parameter
|Name=how
|Data type=any
|Description=Specifies how ''sourceRange'' is compared to the range of the object on which '''compareBoundaryPoints''' is invoked.
|Optional=No
}}{{Method Parameter
|Name=sourceRange
|Data type=any
|Description=[[dom/Range|'''Range''']] object that is compared to the range of the object on which '''compareBoundaryPoints''' is invoked.
|Optional=No
}}
|Method_applies_to=dom/Range
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Returns a –1, 0, or 1 to indicate whether the ''sourceRange'' point is before, equal to, or after the boundary point of the [[dom/Range|'''Range''']] object on which '''compareBoundaryPoints''' is invoked.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
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