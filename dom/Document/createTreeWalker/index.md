{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pRootNode|Data type=Node|Description=The root element or node to start traversing on.|Optional=}}
{{Method Parameter|Name=ulWhatToShow|Data type=Integer|Description=The type of nodes or elements to appear in the node list. For more information, see [[dom/traversal/properties/whatToShow|'''whatToShow''']].|Optional=}}
{{Method Parameter|Name=pFilter|Data type=VARIANT|Description=A custom NodeFilter function to use. For more information, see [[dom/traversal/properties/filter|'''filter''']]. Use a pointer to a null value for no filter.|Optional=}}
{{Method Parameter|Name=fEntityReferenceExpansion|Data type=VARIANT_BOOL|Description=A flag that specifies whether entity reference nodes are expanded. For more information, see [[dom/traversal/properties/expandEntityReferences|'''expandEntityReferences''']].|Optional=}}
{{Method Parameter|Name=ppTreeWalker|Data type=TreeWalker|Description=Returns a [[dom/traversal/TreeWalker|'''TreeWalker''']] object.|Optional=}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|NotSupportedError
|pRootNode is null.
|}
 

[[dom/traversal/TreeWalker|'''TreeWalker''']]

Returns a [[dom/traversal/TreeWalker|'''TreeWalker''']] object.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Use the '''createTreeWalker''' method when you want to navigate a representation of the document's hierarchical structure. If you would rather traverse a sequence of nodes without regard to document structure, use [[dom/traversal/methods/createNodeIterator|'''createNodeIterator''']].
When a custom NodeFilter function isn't needed, use a pointer to a null value rather than just a null value.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[dom/traversal/methods/createNodeIterator|createNodeIterator]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}