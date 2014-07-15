{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=New listing page with proper object capitalization; replaces '''selection'''.
|Checked_Out=Yes
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Selection is the class of the object returned by window.getSelection() and other methods. It represents the text selection in the greater page, possibly spanning multiple elements, when the user drags over static text and other parts of the page. For information about text selection in an individual text editing element, see Input, TextArea and document.activeElement which typically return the parent object returned from window.getSelection().}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=A selection object represents the ranges that the user has selected. Typically, it holds only one range, accessed as follows:
|Code=var selObj {{=}} window.getSelection();
var range  {{=}} selObj.getRangeAt(0);
}}
}}
{{Notes_Section}}
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection Selection Object]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms535869(v=vs.85).aspx Selection Object]
|HTML5Rocks_link=
}}
{{Concept_Listing
|Use_page_title=No
|List_all_subpages=No
}}