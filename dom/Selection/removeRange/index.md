{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Removes a range from a selection.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=range
|Data type=Range
|Description=Range to remove.
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
|Code=/* In gecko Programmaticaly, more than one range can be selected.  
 * This will remove all ranges except the first. see Compatibility Notes below */
selObj {{=}} window.getSelection();
if(selObj.rangeCount > 1) {
 for(var i = 1; i < selObj.rangeCount; i++) {
  selObj.removeRange(selObj.getRangeAt(i));
 }
}
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 9-11 does not currently support multiple or disjointed selections in standards mode.
|Import_Notes====Syntax===
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.removeRange Selection.removeRange]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}