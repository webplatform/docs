{{Page_Title}}
{{Flags
|State=In Progress
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The interface for the primary data type for the entire Document Object Model.}}
{{API_Object
|Subclass_of=dom/EventTarget
|Overview=The '''Node''' interface is the primary datatype for the entire Document Object Model (DOM). It represents a single node in the document tree.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=While all objects implementing the '''Node''' interface expose methods for dealing with children, not all objects implementing the '''Node''' interface may have children. For example, [[html/attributes/text (body element)|'''text''']] nodes may not have children, and adding children to such nodes results in a [[dom/DOMException|'''DOMException''']].
The attributes [[dom/Node/nodeName|'''nodeName''']], [[dom/Node/nodeValue|'''nodeValue''']] and [[dom/Node/attributes|'''attributes''']] are included as a mechanism to get at node information without casting down to the specific derived interface. In cases where there is no obvious mapping of these attributes for a specific [[dom/Node/nodeType|'''nodeType''']] (i.e., '''nodeValue''' for an Element or attributes for a Comment), this returns '''null'''. Note that the specialized interfaces may contain additional and more convenient mechanisms to get and set the relevant information.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core
|Status=Recommendation
|Relevant_changes=Section 1.4
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node Node]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh771916(v=vs.85).aspx Basic DOM Reference]
|HTML5Rocks_link=
}}