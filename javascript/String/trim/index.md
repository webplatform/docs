{{Page_Title}}
{{Flags}}
{{Summary_Section|Removes the leading and trailing white space and line terminator characters from a string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= stringObj.trim()}}
|Values={{JS_Syntax_Parameter
|Name=stringObj
|Required=Required
|Description=A String object or string literal. This string is not modified by the '''trim''' method.}}
}}
{{JS_Return_Value
|Description=The original string with leading and trailing white space and line terminator characters removed.}}
{{Remarks_Section
|Remarks=The characters that are removed include space, tab, form feed, carriage return, and line feed. See Special Characters (Windows Scripting - JScript) for a comprehensive list of white space and line terminator characters.

For an example that shows how to implement your own trim method, see Prototypes and Prototype Inheritance.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''trim''' method.

|Code= var message = "    abc def     \r\n  ";
 
 document.write("[" + message.trim() + "]");
 document.write("&lt;br/&gt;");
 document.write("length: " + message.trim().length);
 
 // Output:
 //  [abc def]
 //  length: 7
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String{{!}}String Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679971(v=vs.94).aspx
|HTML5Rocks_link=
}}