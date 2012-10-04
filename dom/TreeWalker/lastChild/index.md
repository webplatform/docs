{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=oNode|Data type=Node|Description=Object that receives
the last child node in the filtered [[dom/traversal/TreeWalker|'''TreeWalker''']] hierarchy.|Optional=}}
|Method_applies_to=dom/traversal/TreeWalker
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

[[dom/Node|'''Node''']]

Object that receives
the last child node in the filtered [[dom/traversal/TreeWalker|'''TreeWalker''']] hierarchy.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
'''lastChild''' sets the [[dom/traversal/properties/currentNode|'''currentNode''']] to the returned node.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/TreeWalker|TreeWalker]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}