{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Returns a Boolean value that indicates whether the specified command is in the indeterminate state.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=cmdID
|Data type=BSTR
|Description='''String''' that specifies a command identifier.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=document
|Return_value_name=Result
|Javascript_data_type=Boolean
|Return_value_description=Boolean

'''Boolean''' that returns one of the following possible values:

{{{!}} class="wikitable"
{{!}}-
!Return value
!Description
{{!}}-
{{!}}true
{{!}}The command is in the indeterminate state.
{{!}}-
{{!}}false
{{!}}The command is not in the indeterminate state.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=       function SetToBold () {
            if (document.queryCommandIndeterm ("bold")) {
                alert ("The 'bold' command is in an indeterminate state.");
            }
            else {
                if (document.queryCommandState ("bold")) {
                    alert ("The bold formatting will be removed from the selected text.");
                }
                else {
                    alert ("The selected text will be displayed in bold.");
                }
            }
            document.execCommand ('bold', false, null);
        }

}}
}}
{{Notes_Section
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536678(v=vs.85).aspx queryCommandIndeterm Method]
|HTML5Rocks_link=
}}