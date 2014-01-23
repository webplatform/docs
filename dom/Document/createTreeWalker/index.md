{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Creates a [[dom/TreeWalker|'''TreeWalker''']] object that you can use to traverse filtered lists of nodes or elements in a document.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=rootNode
|Data type=String
|Description=The root element or node to start traversing on.
|Optional=No
}}{{Method Parameter
|Name=whatToShow
|Data type=String
|Description=The type of nodes or elements to appear in the node list. For more information, see [[dom/NodeIterator/whatToShow|'''whatToShow''']].
|Optional=No
}}{{Method Parameter
|Name=filter
|Data type=String
|Description=A custom '''NodeFilter''' function to use. For more information, see [[dom/NodeIterator/filter|'''filter''']], or null for none.
|Optional=No
}}{{Method Parameter
|Name=expandEntityReference
|Data type=Boolean
|Description=Whether entity reference nodes are expanded. For more information, see [[dom/NodeIterator/expandEntityReferences|'''expandEntityReferences''']].
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=treeWalker
|Javascript_data_type=DOM Node
|Return_value_description=A [[dom/TreeWalker|'''TreeWalker''']] instance object.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use the '''createTreeWalker''' method when you want to navigate a representation of the document's hierarchical structure. If you would rather traverse a sequence of nodes without regard to document structure, use [[dom/NodeIterator/createNodeIterator|'''createNodeIterator''']].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Traversal and Range
|URL=http://www.w3.org/TR/DOM-Level-2-Traversal-Range/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/NodeIterator/createNodeIterator|createNodeIterator]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}