{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the end of a range to a point after a specific node.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=referenceNode
|Data type=DOM Node
|Description=A node in the document hierarchy.
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
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();
var referenceNode {{=}} document.getElementsByTagName("div").item(0);

range.setEndAfter(referenceNode);
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
range.setEndAfter(referenceNode);
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-setendafter
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.setEndAfter Range.setEndAfter]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975449(v=vs.85).aspx setEndAfter Method]
|HTML5Rocks_link=
}}