{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the parent object in the document hierarchy relative to the current node and updates currentNode.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/TreeWalker
|Example_object_name=treewalker
|Return_value_name=node
|Javascript_data_type=DOM Node
|Return_value_description=Object that receives the parent node in the filtered TreeWalker hierarchy. 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var treewalker {{=}} document.createTreeWalker(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
var node {{=}} treewalker.parentNode(); // returns null as there is no parent
}}
}}
{{Notes_Section
|Notes====Remarks===
'''parentNode''' sets the [[dom/TreeWalker/currentNode|'''currentNode''']] to the returned node.

 If no such node exists, or if it is above the TreeWalker's root node, returns null and the current node is not changed.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-treewalker-parentnode
|Status=Living Standard
|Relevant_changes=No Change
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.parentNode TreeWalker.parentNode
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974805(v=vs.85).aspx parentNode Method]
|HTML5Rocks_link=
}}