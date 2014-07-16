{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Replaces the current selection with an empty selection (or a caret) at the given offset.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=parentNode
|Data type=DOM Node
|Description=The parent node that the selection is contained in.
|Optional=No
}}{{Method Parameter
|Name=offset
|Data type=Number
|Description=The number of units from the start in which to place the caret or collapsed selection.
|Optional=No
}}
|Method_applies_to=dom/Selection
|Example_object_name=selObj
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Place the caret at the beginning of an HTML document's body.
|Code=var body {{=}} document.getElementsByTagName('body')[0];
var selObj{{=}}window.getSelection();
selObj.collapse(body,0);
}}
}}
{{Notes_Section
|Notes====Remarks===
Raises a WRONG_DOCUMENT_ERR [[dom/DOMException|'''DOMException''']] if the ''parentNode'' is in another document.
|Import_Notes====Syntax===
selObj.collapse(parentNode, offset);
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.1
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.collapse Selection.collapse]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975173(v=vs.85).aspx collapse Method]
|HTML5Rocks_link=
}}