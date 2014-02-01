{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the string value of an error.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= error.valueOf()}}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The error object is any instance of an Error.}}
}}
{{JS_Return_Value
|Description=The string "Error: " plus the error message.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''valueOF''' method with a date.

|Code= var myError = new Error();
 myError.message = "This is an error.";
 var value = myError.valueOf();
 document.write(value);
 
 // Output: Error: This is an error.
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155293(v=vs.94).aspx
|HTML5Rocks_link=
}}