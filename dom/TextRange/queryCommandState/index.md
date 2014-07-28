{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Returns a Boolean value that indicates the current state of the command.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=cmdID
|Data type=BSTR
|Description='''String''' that specifies a command identifier.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=document
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=Boolean

'''Boolean''' that returns one of the following possible values:

{{{!}} class="wikitable"
{{!}}-
!Return value
!Description
{{!}}-
{{!}}true
{{!}}The given command has been executed on the object.
{{!}}-
{{!}}false
{{!}}The given command has not been executed on the object.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example feature tests for window.getSelection and if not available (legacy IE versions) falls back to document.selection to create a range object. Then queryCommandState is used to determine if the range object can execute the 'bold' command.
|Code=function makeBold(el){
if(window.getSelection){
	var sel{{=}}document.getSelection();
	var range {{=}} sel.getRangeAt(0),
  	content {{=}} range.extractContents(),
    span {{=}} document.createElement('b');
	span.appendChild(content);
	var htmlContent {{=}} span.innerHTML;
	range.insertNode(span);
}else{
	var sel{{=}}document.selection;
	if(sel){
		var rng{{=}}sel.createRange();
		if(rng.queryCommandEnabled('bold')){rng.execCommand('bold',false,null);}
	}	
}
}

}}
}}
{{Notes_Section
|Usage=Used to add HTML markup to web documents.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536679(v=vs.85).aspx queryCommandState Method]
|HTML5Rocks_link=
}}