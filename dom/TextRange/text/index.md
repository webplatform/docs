{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Not sure if a standard applies here.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Mixed}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the text contained within the range. }}
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
{{Notes_Section
|Usage=Used to extract only the text content from a range.
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534676(v=vs.85).aspx text Property]
|HTML5Rocks_link=
}}