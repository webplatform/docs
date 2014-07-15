{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the end point of the range.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=endNode
|Data type=DOM Node
|Description=A node in the document hierarchy.
|Optional=No
}}{{Method Parameter
|Name=offset
|Data type=Number
|Description=Specifies the offset value for the end point.
|Optional=No
}}
|Method_applies_to=dom/Range
|Example_object_name=range
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
{{!}}W3Exception_DOM_INDEX_SIZE_ERR
{{!}}offset is negative or greater than the number of child units in refNode.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();
var endNode {{=}} document.getElementsByTagName("p").item(3);
var endOffset {{=}} document.getElementsByTagName("p").item(3).childNodes.length;
range.setEnd(endNode,endOffset);
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
range.setEnd(endNode, endOffset);
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-setend
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.setEnd Range.setEnd]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975448(v=vs.85).aspx setEnd Method]
|HTML5Rocks_link=
}}