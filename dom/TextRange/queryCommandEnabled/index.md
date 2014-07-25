{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Returns a Boolean value that indicates whether a specified command can be successfully executed using execCommand, given the current state of the document.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=cmdID
|Data type=BSTR
|Description='''String''' that specifies a command identifier.

see [http://help.dottoro.com/larpvnhw.php dottoro.com] for a full listing of commands.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=document
|Return_value_name=Restult
|Javascript_data_type=Boolean
|Return_value_description=Boolean

'''Boolean''' that returns one of the following possible values:

{{{!}} class="wikitable"
{{!}}-
!Return value
!Description
{{!}}-
{{!}}true
{{!}}The command is enabled.
{{!}}-
{{!}}false
{{!}}The command is disabled.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example is a onClick handler to execute the 'cut' command.
|Code=function execCut(){
if(document.queryCommandEnabled('cut')){
	document.execCommand('cut',false,null);}
}
}}
}}
{{Notes_Section
|Notes====Remarks===
Using '''queryCommandEnabled''' ("delete") on a [[dom/TextRange|'''TextRange''']] object returns true, while '''queryCommandEnabled''' ("delete") on a [[dom/Document|Document]] object returns false. However, '''execCommand''' ("delete") can still be used to delete the selected text.
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
{{See_Also_Section
|Manual_links=[http://help.dottoro.com/larpvnhw.php help.dottoro.com - Command Reference]

[http://msdn.microsoft.com/en-us/library/ie/hh801227(v=vs.85).aspx MSDN Commands A-Z]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536676(v=vs.85).aspx queryCommandEnabled Method]
|HTML5Rocks_link=
}}