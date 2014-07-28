{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Returns a Boolean value that indicates whether the current command is supported on the current range.}}
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
{{!}}The command is supported.
{{!}}-
{{!}}false
{{!}}The command is not supported.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The follow example uses window.getSelection feature testing and if it is not supported by the client browser falls back to document.selection. 'queryCommandSupported' is then used on the range object to determine if the 'bold' command is supported in the current context.
|Code=function makeBold(el){
if(window.getSelection){
	var sel=document.getSelection();
	var range = sel.getRangeAt(0),
  	content = range.extractContents(),
    span = document.createElement('b');
	span.appendChild(content);
	var htmlContent = span.innerHTML;
	range.insertNode(span);
}else{
	var sel=document.selection;
	if(sel){
		var rng=sel.createRange();
		if(rng.queryCommandSupported('bold')){
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536681(v=vs.85).aspx queryCommandSupported Method]
|HTML5Rocks_link=
}}