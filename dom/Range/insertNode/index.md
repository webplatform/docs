{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Inserts a node into the start of a Range object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=oNode
|Data type=DOM Node
|Description=The new node to insert.
|Optional=No
}}
|Method_applies_to=dom/Range
|Example_object_name=newNode
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code
!Description
{{!}}-
{{!}}S_OK
{{!}}The operation completed successfully.
{{!}}-
{{!}}InvalidStateError
{{!}}detach has been invoked on the object.
{{!}}-
{{!}}W3Exception_DOM_HIERARCHY_REQUEST_ERR
{{!}}newNode is an ancestor of the container, or the container type for the start of the range does not allow children of type newNode.
{{!}}-
{{!}}W3Exception_DOM_WRONG_DOCUMENT_ERR
{{!}}newNode and the container for the start of the range were not created from the same document.
{{!}}-
{{!}}W3Exception_DOM_NO_MODIFICATION_ALLOWED_ERR
{{!}}A  node or portion of the content in the range is read-only.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();
newNode {{=}} document.createElement("p");
newNode.appendChild(document.createTextNode("New Node Inserted Here"));
range.selectNode(document.getElementsByTagName("div").item(0));
range.insertNode(newNode);
}}
}}
{{Notes_Section
|Notes====Remarks===
If the container is of type  [[dom/TextNode|'''TextNode''']], '''insertNode''' splits the text node, and inserts ''newNode'' between the resulting two text nodes.
If ''newNode'' is a document fragment, the children of the document fragment node are inserted rather than the ''newNode'' itself.
|Import_Notes====Syntax===
range.insertNode(newNode);
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-insertnode
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.insertNode Range.insertNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975445(v=vs.85).aspx insertNode Method]
|HTML5Rocks_link=
}}