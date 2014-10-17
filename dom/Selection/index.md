{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=New listing page with proper object capitalization; replaces '''selection'''.
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Represents the text selection in the greater page, possibly spanning multiple elements, when the user drags over static text and other parts of the page.}}
{{API_Object
|Subclass_of=
|Overview=Selection is the class of the object returned by [[dom/Window/getSelection|window.getSelection()]] and other methods. For information about text selection in an individual text editing element, see [[dom/HTMLInputElement|Input]], [[dom/HTMLTextAreaElement|TextArea]] and [[dom/Document/activeElement|document.activeElement]] which typically return the parent object returned from window.getSelection().
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=A selection object represents the ranges that the user has selected. Typically, it holds only one range, accessed as follows:
|Code=var selObj {{=}} window.getSelection();
if(selObj.rangeCount){ range  {{=}} selObj.getRangeAt(0);}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Proposed Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection Selection Object]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974359(v=vs.85).aspx HTMLSelection Object]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}



{{Concept_Listing
|Use_page_title=No
|List_all_subpages=No
}}