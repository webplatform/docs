{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a string representation of an error.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=error.toString()
}}
|Values={{JS Syntax Parameter
|Name=date
|Required=Required
|Description=The error to represent as a string.
}}
}}
{{JS_Return_Value
|Description=Returns "Error: " plus the error message.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toString''' method with an error.
|Code=var myError = new Error();
 myError.message = "My Error";
 var errorString = myError.toString();
 document.write(errorString);
 
 // Output: Error: My Error
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155283(v=vs.94).aspx
|HTML5Rocks_link=
}}