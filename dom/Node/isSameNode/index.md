{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Determines if two nodes are the same node.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=otherNode
|Data type=DOM Node
|Description=The node to be compared to the node that is executing the method.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=isSame
|Javascript_data_type=Boolean
|Return_value_description=Whether the node specified in the otherNode parameter refers to the same node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following example isSameNode is false since
document.body is the body node while document.documentElement is the html node.
|Code=var isSameNode = document.body..isSameNode(document.documentElement);
}}
}}
{{Notes_Section
|Usage=This determines whether or not two references refer to the same node.  If the references refer to the same node, you can use the references interchangeably, even when using a proxy.
|Notes=Obsolete
This feature is obsolete. Although it may still work in some browsers, its use is discouraged since it could be removed at any time. Try to avoid using it.
In browsers where isSameNode is no longer supported 
// Instead of using
node1.isSameNode(node2)

// use
node1 {{===}} node2 // or
node1 {{==}} node2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=DOM Level 4 Core
|URL=http://www.w3.org/TR/domcore/
|Status=Recommendation
|Relevant_changes=9.2 DOM Core
}}
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.isSameNode Node.isSameNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975129(v=vs.85).aspx isSameNode Method]
|HTML5Rocks_link=
}}