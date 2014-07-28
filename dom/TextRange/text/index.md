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
{{API_Object_Property
|Property_applies_to=dom/TextRange
|Read_only=No
|Example_object_name=textRange
|Return_value_name=result
|Javascript_data_type=String
|Return_value_description=the contained text.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example feature tests for document.selection, and if a selection has been made in the document, displays the text content of the selection in an alert box.
|Code=if(document.selection){
var sel{{=}}document.selection;
var rng{{=}}sel.createRange();
if(!rng){alert(rng.text);

}
}}{{Single Example
|Language=JavaScript
|Description=The following example uses the text property of a textRange to insert a bounding &lt;u&gt; tag around the selected text.
|Code=if(document.selection){
	var sel{{=}}document.selection;
	if(sel){
		var rng{{=}}sel.createRange();
		if(rng!{{=}}null){
			rng.pasteHTML('<u>'+rng.text+'</u>');
			showTextRangeProp(rng);
		}
		}
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The text formats within the current context of the document. You cannot set this property while the document is loading. Wait for the [[dom/Element/load|'''onload''']] event before attempting to set this property.
This feature might not be available on non-Microsoft Win32 platforms.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534676(v=vs.85).aspx text Property]
|HTML5Rocks_link=
}}