{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the string value of an error.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=error.valueOf()
}}
|Values=
}}
{{JS_Return_Value
|Description=The string "Error: " plus the error message. 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''valueOF''' method with a date.
|Code=var myError = new Error();
 myError.message = "This is an error.";
 var value = myError.valueOf();
 document.write(value);
 
 // Output: Error: This is an error.
}}
}}
{{Remarks_Section
|Remarks=The error object is any instance of an Error.
}}
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155293(v=vs.94).aspx
|HTML5Rocks_link=
}}