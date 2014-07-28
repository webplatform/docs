{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Returns the current value of the document, range, or current selection for the given command.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=cmdID
|Data type=BSTR
|Description='''String''' that specifies a command identifier.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=document
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Variant

'''Variant''' that returns the command value for the document, range, or current selection, if supported. Possible values  depend on ''cmdID''. If not supported, this method returns a '''Variant''' of type '''Boolean''' set to false.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example when using legacy document.selection will display an alert message of 'false' if the current selection is not 'bold', or true if it is already 'bold'
|Code=function makeBold(el){
if(window.getSelection){
	var sel{{=}}document.getSelection();
	var range{{=}} sel.getRangeAt(0),
  	content {{=}} range.extractContents(),
    span {{=}} document.createElement('b');
	span.appendChild(content);
	var htmlContent {{=}} span.innerHTML;
	range.insertNode(span);
}else{
	var sel{{=}}document.selection;
	if(sel){
		var rng{{=}}sel.createRange();
		alert(rng.queryCommandValue('bold'));
// true if the rng is 'bold' already, false otherwise.
		if(rng.queryCommandSupported('bold')){
			if(rng.queryCommandEnabled('bold')){rng.execCommand('bold',false,null);}
		}
	}	
}
}

}}
}}
{{Notes_Section
|Usage=Used for changing the HTML markup of web pages.
|Notes====Remarks===
This method is a wrapper function for the command constants. You can obtain an '''IHTMLDocument2''' interface using IID_IHTMLDocument2 for the IID.
This method is a wrapper function for the command constants. You can obtain an '''IHTMLControlRange''' interface using IID_IHTMLControlRange for the IID.
This method is a wrapper function for the command constants. You can obtain an '''IHTMLTxtRange''' interface using IID_IHTMLTxtRange for the IID.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536683(v=vs.85).aspx queryCommandValue Method]
|HTML5Rocks_link=
}}