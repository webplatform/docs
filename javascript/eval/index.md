{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Evaluates JavaScript code and executes it.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=eval( codeString )
}}
|Values={{JS Syntax Parameter
|Name=codeString
|Required=Required
|Description=A '''String''' value that contains valid JavaScript code.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code initializes the variable <code>myDate</code> to a test date.
|Code=var dateFn = "Date(1971,3,8)";
 var myDate;
 eval("myDate = new " + dateFn + ";");
 
 document.write(myDate);
 
 // Output: Thu Apr 8 00:00:00 PDT 1971
}}
}}
{{Remarks_Section
|Remarks=The '''eval''' function enables dynamic execution of JavaScript source code.

The codeString string is parsed by the JavaScript parser and executed.

The code passed to the '''eval''' function is executed in the same context as the call to the '''eval''' function.

Whenever possible, use the [[javascript/JSON/parse{{!}}JSON.parse function]] to de-serialize JavaScript Object Notation (JSON) text. The '''JSON.parse''' function is more secure and executes faster than the '''eval''' function.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/String{{!}}String Object]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/12k71sw7(v=vs.94).aspx
|HTML5Rocks_link=
}}