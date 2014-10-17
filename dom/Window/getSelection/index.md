{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a [[dom/Selection|Selection] object that represents the current selection of the document.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Window
|Example_object_name=window
|Return_value_name=selection
|Javascript_data_type=Object
|Return_value_description=A [[dom/Selection|Selection]] object that represents the currently selected text in the window.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=function foo() {
    var selObj {{=}} window.getSelection(); 
    alert(selObj);
    var selRange {{=}} selObj.getRangeAt(0);
    // do stuff with the range
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 6.6.1
}}
{{Related_Specifications_Section
|Specifications=
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.getSelection getSelection]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975169(v=vs.85).aspx getSelection Method]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}