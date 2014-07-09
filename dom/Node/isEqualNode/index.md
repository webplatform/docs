{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Determines whether two nodes are equal in their type, name and namespace.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=otherNode
|Data type=DOM Node
|Description=The node to be compared to the node that is executing the method.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=isEqual
|Javascript_data_type=Boolean
|Return_value_description=Whether the node specified in the ''otherNode'' parameter is equal to the current node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the follow example if #targetElm is the first div element of the document 'true' will be displayed.
|Code=var targetElm {{=}} document.getElementById("targetElm");
var firstDiv {{=}} document.getElementsByTagName("div")[0];

alert( targetElm.isEqualNode(firstDiv) );
}}
}}
{{Notes_Section
|Usage=This method determines whether or not two nodes are equal.  Nodes are considered equal when the values of the following attributes are equal:
*[[dom/Node/nodeType|'''nodeType''']]
*[[dom/Node/nodeName|'''nodeName''']]
*[[dom/Node/localName|'''localName''']]
*[[dom/Node/namespaceURI|'''namespaceURI''']]
|Notes=Nodes can be equal without being the same.  Use [[dom/Node/isSameNode|'''isSameNode''']] to determine if two nodes are the same.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.isEqualNode Node.isEqual]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975128(v=vs.85).aspx isEqualNode Method]
|HTML5Rocks_link=
}}