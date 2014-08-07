{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=ppIHTMLSelection
|Data type=any
|Description=An [[dom/HTMLSelection|'''HTMLSelection''']] object that represents the current selection, if any.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=object
|Return_value_name=selObj
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=function foo() {
    var selObj {{=}} window.getSelection(); 
    alert(selObj);
    var selRange {{=}} selObj.getRangeAt(0);
    // do stuff with the range
}
}}
}}
{{Notes_Section
|Usage=HTML Editing API's
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 6.6.1
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.getSelection getSelection]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975169(v=vs.85).aspx getSelection Method]
|HTML5Rocks_link=
}}