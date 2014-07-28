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
|Description=The following example feature tests for getSelection support and extracts the text contained within the bounds of the range(s) object(s).
|Code=function showText(){
if(window.getSelection){
	var buf{{=}}'';
	var sel{{=}}document.getSelection();
	for(var I{{=}}0;i<sel.rangeCount;i++)
	{
		var range{{=}}sel.getRangeAt(i);
		buf+{{=}}range.extractContents().textContent;
	}
	alert(buf);
}else{
	var sel{{=}}document.selection;
	if(sel){
		var rng{{=}}sel.createRange();
		if(rng!{{=}}null){
			alert(rng.text);
		}
		}
}
}


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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}