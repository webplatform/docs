{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The NodeIterator.whatToShow read-only property represents an unsigned integer representing a bitmask signifying what types of nodes should be returned by the NodeIterator.}}
{{API_Object_Property
|Property_applies_to=dom/NodeIterator
|Read_only=Yes
|Return_value_name=nodeTypes
|Javascript_data_type=unsigned long
|Return_value_description=The type of accepted nodes.p is a bitwise OR of the following values:

NodeFilter.SHOW_ALL (0xFFFFFFFF) Show all nodes.

NodeFilter.SHOW_ELEMENT (0x00000001) Show Element nodes.

NodeFilter.SHOW_ATTRIBUTE (0x00000002) show Attribute nodes. 

NodeFilter.SHOW_TEXT (0x00000004) Show Text nodes.

NodeFilter.SHOW_CDATA_SECTION (0x00000008)
Show CDATASection nodes.

NodeFilter.SHOW_ENTITY_REFERENCE (0x00000010)
Show EntityReference nodes.

NodeFilter.SHOW_ENTITY (0x00000020)
Show Entity nodes.

NodeFilter.SHOW_PROCESSING_INSTRUCTION (0x00000040)
Show ProcessingInstruction nodes.

NodeFilter.SHOW_COMMENT (0x00000080)
Show Comment nodes.

NodeFilter.SHOW_DOCUMENT (0x00000100)
Show Document nodes.

NodeFilter.SHOW_DOCUMENT_TYPE (0x00000200)
Show DocumentType nodes.

NodeFilter.SHOW_DOCUMENT_FRAGMENT (0x00000400)
Show DocumentFragment nodes.

NodeFilter.SHOW_NOTATION (0x00000800)
Show Notation nodes.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var nodeIterator {{=}} document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT + NodeFilter.SHOW_COMMENT + NodeFilter.SHOW_TEXT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
if( (nodeIterator.whatToShow == NodeFilter.SHOW_ALL) ||
    (nodeIterator.whatToShow % (NodeFilter.SHOW_COMMENT*2)) >= NodeFilter.SHOW_COMMENT) {
    // nodeIterator will show comments
}
}}
}}
{{Notes_Section
|Notes====Remarks===
Filtering is based both on the '''whatToShow''' flags and the [[dom/NodeIterator/filter|'''filter''']] function.
|Import_Notes====Syntax===
var nodeTypes = nodeIterator.whatToShow;
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-nodeiterator-whattoshow
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.whatToShow NodeIterator.whatToShow]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974822(v=vs.85).aspx whatToShow Property]
|HTML5Rocks_link=
}}