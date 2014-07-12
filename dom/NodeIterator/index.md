{{Page_Title}}
{{Flags
|State=In Progress
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The NodeIterator interface represents an iterator over the members of a list of the nodes in a subtree of the DOM. The nodes will be returned in document order.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var nodeIterator {{=}} document.createNodeIterator(root, whatToShow, filter);
}}
}}
{{Notes_Section
|Usage=Used in web browser Developer Tools UI to provide a consistent and interoperable means of traversing DOM Nodes.
|Notes====Remarks===
The '''NodeIterator''' is dynamic, reflecting the state of the document as it is edited or changed.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator NodeIterator]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974357(v=vs.85).aspx nodeIterator Object]
|HTML5Rocks_link=
}}