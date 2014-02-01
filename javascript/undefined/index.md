{{Page_Title}}
{{Flags}}
{{Summary_Section|A value that has never been defined, such as a variable that has not been initialized.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= undefined}}
}}
{{Remarks_Section
|Remarks=The '''undefined''' constant is a member of the '''Global''' object, and becomes available when the scripting engine is initialized. When a variable has been declared but not initialized, its value is '''undefined'''.

If a variable has not been declared, you cannot compare it to '''undefined''' , but you can compare the type of the variable to the string "undefined".

The '''undefined''' constant is useful when explicitly testing or setting a variable to undefined.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''undefined''' constant.

|Code= // A variable that has not been initialized.
 var declared;
 
 if (declared == undefined)
     document.write("declared has not been given a value &lt;br/&gt;");
 else
     document.write("declared has been given a value &lt;br/&gt;");
 
 document.write("typeof declared is " + typeof(declared) + "&lt;br/&gt;");
 
 // An undeclared variable cannot be compared to undefined,
 // so the next line would generate an error.
 // if (notDeclared == undefined);
 
 document.write("typeof notDeclared is " + typeof(notDeclared));
 
 // Output:
 // declared has not been given a value
 // typeof declared is undefined
 // typeof notDeclared is undefined
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/typeof{{!}}typeof Operator]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dae3sbk5(v=vs.94).aspx
|HTML5Rocks_link=
}}