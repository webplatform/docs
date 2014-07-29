{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the previous sibling of the current node in the filtered TreeWalker hierarchy and updates currentNode.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/TreeWalker
|Example_object_name=treewalker
|Return_value_name=node
|Javascript_data_type=DOM Node
|Return_value_description=.Object that receives the previous child of a parent node in the filtered TreeWalker hierarchy. 
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
var node {{=}} treewalker.previousSibling(); // returns null as there is no previous sibiling
}}
}}
{{Notes_Section
|Notes====Remarks===
'''previousSibling''' sets the [[dom/TreeWalker/currentNode|'''currentNode''']] to the returned node. It 
returns null if there are no more child nodes.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-treewalker-previoussibling
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.previousSibling TreeWalker.previousSibling]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975265(v=vs.85).aspx previousSibling Method]
|HTML5Rocks_link=
}}