{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=oNode|Data type=Node|Description=Node
in the document hierarchy.|Optional=}}
{{Method Parameter|Name=offset|Data type=Integer|Description=Specifies the offset value for the starting point.|Optional=}}
|Method_applies_to=dom/traversal/Range
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
|W3Exception_DOM_INDEX_SIZE_ERR
|offset is negative or greater than the number of child units in refNode.
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
|W3Exception_DOM_INDEX_SIZE_ERR
|offset is negative or greater than the number of child units in refNode.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
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