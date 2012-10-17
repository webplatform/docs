{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=apis/EventTarget
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''Node''' interface is the primary datatype for the entire Document Object Model (DOM). It represents a single node in the document tree. While all objects implementing the '''Node''' interface expose methods for dealing with children, not all objects implementing the '''Node''' interface may have children. For example, [[html/attributes/text (body element)|'''text''']] nodes may not have children, and adding children to such nodes results in a [[dom/DOMException|'''DOMException''']].
The attributes [[dom/properties/nodeName|'''nodeName''']], [[dom/properties/nodeValue|'''nodeValue''']] and [[dom/properties/attribute|'''attributes''']] are included as a mechanism to get at node information without casting down to the specific derived interface. In cases where there is no obvious mapping of these attributes for a specific [[dom/properties/nodeType|'''nodeType''']] (i.e., '''nodeValue''' for an Element or attributes for a Comment), this returns '''null'''. Note that the specialized interfaces may contain additional and more convenient mechanisms to get and set the relevant information.
|Import_Notes====Members===
The '''Node''' object does not define any members.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/Element|Element]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}