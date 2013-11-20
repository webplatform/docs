{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=oNode|Data type=Node|Description=The
new node
to insert.|Optional=}}
|Method_applies_to=dom/Range
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|InvalidStateError
|detach has been invoked on the object.
|-
|W3Exception_DOM_HIERARCHY_REQUEST_ERR
|newNode is an ancestor of the container, or the container type for the start of the range does not allow children of type newNode.
|-
|W3Exception_DOM_WRONG_DOCUMENT_ERR
|newNode and the container for the start of the range were not created from the same document.
|-
|W3Exception_DOM_NO_MODIFICATION_ALLOWED_ERR
|A  node or portion of the content in the range is read-only.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|InvalidStateError
|detach has been invoked on the object.
|-
|W3Exception_DOM_HIERARCHY_REQUEST_ERR
|newNode is an ancestor of the container, or the container type for the start of the range does not allow children of type newNode.
|-
|W3Exception_DOM_WRONG_DOCUMENT_ERR
|newNode and the container for the start of the range were not created from the same document.
|-
|W3Exception_DOM_NO_MODIFICATION_ALLOWED_ERR
|A  node or portion of the content in the range is read-only.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
If the container is of type  [[dom/TextNode|'''TextNode''']], '''insertNode''' splits the text node, and inserts ''newNode'' between the resulting two text nodes.
If ''newNode'' is a document fragment, the children of the document fragment node are inserted rather than the ''newNode'' itself.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/Range|Range]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}