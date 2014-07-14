{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Removes the contents of a range from a document or document fragment and puts it a new document fragment.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=oDocumentFragment
|Data type=any
|Description=Returns an object that contains the extracted content.
|Optional=No
}}
|Method_applies_to=dom/Range
|Example_object_name=range
|Return_value_name=documentFragment
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
{{!}}-
{{!}}W3Exception_DOM_NO_MODIFICATION_ALLOWED_ERR
{{!}}A  node or portion of the content in the range is read-only.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=range {{=}} document.createRange();
range.selectNode(document.getElementsByTagName("div").item(0));
documentFragment {{=}} range.extractContents();
document.body.appendChild(documentFragment);
}}
}}
{{Notes_Section
|Notes=Event Listeners added using DOM Events are not retained during extraction. HTML attribute events are retained or duplicated as they are for the Node.cloneNode() method. HTML id attributes are also cloned, which can lead to an invalid document if a partially-selected node is extracted and appened to the document.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-extractcontents
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.extractContents Range.extractContents]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975443(v=vs.85).aspx extractContents Method]
|HTML5Rocks_link=
}}