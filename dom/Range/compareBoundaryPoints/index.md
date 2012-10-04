{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=how|Data type=short|Description=Specifies how ''sourceRange'' is compared to the range of the object on which '''compareBoundaryPoints''' is invoked.|Optional=}}
{{Method Parameter|Name=sourceRange|Data type=object|Description=[[dom/traversal/Range|'''Range''']] object

 that is compared to the range of the object on which '''compareBoundaryPoints''' is invoked.|Optional=}}
|Method_applies_to=dom/traversal/Range
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''Integer'''

Returns a –1, 0, or 1 to indicate whether the ''sourceRange'' point is before, equal to, or after the boundary point of the [[dom/traversal/Range|'''Range''']] object on which '''compareBoundaryPoints''' is invoked.


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/Range|Range]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}