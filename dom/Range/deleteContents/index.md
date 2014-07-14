{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Removes all contents within a selected range. }}
{{API_Object_Method
|Parameters=
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
{{!}}W3Exception_DOM_NO_MODIFICATION_ALLOWED_ERR
{{!}}Some of the contents or nodes are read-only.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
If the deleted range contains closing or opening tags, the remaining tags are completed.
|Import_Notes====Syntax===
Range.deleteContents(); 
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 2.13
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-deletecontents
|Status=Living Standard
|Relevant_changes=No change
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.deleteContents Range.deleteContents]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975441(v=vs.85).aspx deleteContents Method]
|HTML5Rocks_link=
}}