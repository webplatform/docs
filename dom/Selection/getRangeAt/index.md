{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns a specified Range from a selection. The Range is specified by an index and cannot be greater than the number that is returned by rangeCount. }}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=index
|Data type=Number
|Description=The zero-based index of the range to return. A negative number or a number greater than or equal to rangeCount will result in an error.
|Optional=No
}}
|Method_applies_to=dom/Selection
|Example_object_name=selObj
|Return_value_name=range
|Javascript_data_type=Range
|Return_value_description=The range object that will be returned.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var ranges {{=}} [];

var selObj {{=}} window.getSelection();

for(var i {{=}} 0; i < selObj.rangeCount; i++) {
 ranges[i] {{=}} selObj.getRangeAt(i);
}
/* Each item in the ranges array is now 
 * a range object representing one of the 
 * ranges in the current selection */
}}
}}
{{Notes_Section
|Notes====Remarks===
Currently only Gecko supports multiple or disjointed selections.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.getRangeAt Selection.getRangeAt]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975177(v=vs.85).aspx getRangeAt Method]
|HTML5Rocks_link=
}}