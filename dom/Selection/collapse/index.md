{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=The previous note said -
MSDN documentation is incorrect.
offset may have 0 or 1 value;

offset
    0 - Collapses the selection from the anchor to the beginning of parentNode's text.
    1 - Collapses the selection from the anchor to the end of parentNode's text.

However, testing in Chrome, values other than 0 or 1 are supported and are affecting the position of the caret accordingly.
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
|Description={{TODO|Verify these values, as Chrome seems to respect values other than 0 or 1 and act accordingly.}}
    0 - Collapses the selection from the anchor to the beginning of parentNode's text.
    1 - Collapses the selection from the anchor to the end of parentNode's text.
|Optional=No
}}
|Method_applies_to=dom/Selection
|Example_object_name=selObj
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Place the caret at the beginning of an HTML document's body.
|Code=var body {{=}} document.getElementsByTagName('body')[0];
var selObj {{=}} window.getSelection();
selObj.collapse(body,0);// offset 0
}}
}}
{{Notes_Section
|Notes=Throws a WrongDocumentError [[dom/DOMException|'''DOMException''']] if the ''parentNode'' is in another document.
Throws a TypeError [[dom/DOMException|'''DOMException''']] if the relevantly typed arguments are not specified.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML Editing APIs
|URL=https://dvcs.w3.org/hg/editing/raw-file/tip/editing.html#dom-selection-collapse
|Status=W3C Community Group Work In Progress
}}{{Related Specification
|Name=HTML5 (Expired)
|URL=http://www.w3.org/TR/2010/WD-html5-20100624/editing.html#selection-0
|Status=W3C Working Draft (Expired)
|Relevant_changes=7.6.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=34 and earlier
|Note=The arguments were optional and so no TypeError was thrown.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9 and earlier
|Note=For `parentNode` from another document, a WRONG_DOCUMENT_ERR exception is thrown instead of a WrongDocumentError exception.
}}
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