{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a document fragment containing the nodes of a range. If any nodes are partially selected, their start or end nodes are included.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=oDocumentFragment
|Data type=any
|Description=Returns a document fragment object.
|Optional=No
}}
|Method_applies_to=dom/Range
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
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
{{!}}A  document type node is included in the range  that is being cloned.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();
range.selectNode(document.getElementsByTagName("div").item(0));
var documentFragment {{=}} range.cloneContents();
document.body.appendChild(documentFragment);
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
documentFragment = range.cloneContents();
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.cloneContents Range.cloneContents]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975437(v=vs.85).aspx cloneContents Method]
|HTML5Rocks_link=
}}