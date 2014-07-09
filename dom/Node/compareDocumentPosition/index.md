{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Compares the position of two nodes in a document.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=otherNode
|Data type=DOM Node
|Description=The node to be compared to the reference node, which is the node executing the method.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=positionBitmask
|Javascript_data_type=Number
|Return_value_description=Describes how the position of the node specified by the ''otherNode'' parameter relates to the position of the reference node. The return value contains one or more of the following flag values:

{{{!}} class="wikitable"
{{!}}-
![[dom/Node|Node]] constant name
!Return value (Integer)
!Return value (Hexadecimal)
!Description
{{!}}-
{{!}}DOCUMENT_POSITION_DISCONNECTED 
{{!}}1
{{!}}0x01
{{!}}The nodes are disconnected.
{{!}}-
{{!}}DOCUMENT_POSITION_PRECEDING
{{!}}2
{{!}}0x02
{{!}}The position of the node specified by the otherNode parameter precedes the position of the reference node.
{{!}}-
{{!}}DOCUMENT_POSITION_FOLLOWING
{{!}}4
{{!}}0x04
{{!}}The position of the node specified by the otherNode parameter follows the position of the reference node.
{{!}}-
{{!}}DOCUMENT_POSITION_CONTAINS
{{!}}8
{{!}}0x08
{{!}}The reference node contains the node specified by the otherNode parameter.
{{!}}-
{{!}}DOCUMENT_POSITION_CONTAINED_BY
{{!}}16
{{!}}0x10
{{!}}The node specified by the otherNode parameter contains the reference node.
{{!}}-
{{!}}DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC
{{!}}32
{{!}}0x20
{{!}}The node positions depend on the DOM implementation and cannot be compared.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example determines if the web document is incorrectly marked up with the body element before the head element.
Note: Web browsers sometimes self correct markup errors. HTML5 is the first specification to give guidelines to browser vendors on how they should correct markup errors.
|Code=var head = document.getElementsByTagName('head').item(0);
if (head.compareDocumentPosition(document.body) & Node.DOCUMENT_POSITION_FOLLOWING) {
  console.log("well-formed document");
} else {
  console.log("<head> is not before <body>");
}
}}
}}
{{Notes_Section
|Notes=For information about the factors that affect the position of nodes within the DOM, see the related specifications.
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
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.compareDocumentPosition Node.compareDocumentPosition]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975125(v=vs.85).aspx compareDocumentPosition Method]
|HTML5Rocks_link=
}}