{{Page_Title}}
{{Flags}}
{{Summary_Section|Declares a new function.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= function functionname ([ arg1 [, arg2 [,...[, argN ]]]] ''')''' {}}{{JS_Syntax_Format
|Format=     statements }}{{JS_Syntax_Format
|Format= } }}
|Values={{JS_Syntax_Parameter
|Name=functionname
|Required=Required
|Description=The name of the function.}}{{JS_Syntax_Parameter
|Name=arg1...argN
|Required=Optional
|Description=An optional, comma-separated list of arguments the function understands.}}{{JS_Syntax_Parameter
|Name=statements
|Required=Optional
|Description=One or moreJavaScript statements.}}
}}
{{Remarks_Section
|Remarks=Use the function statement to declare a function for later use. The code that is contained in statements is not executed until the function is called from elsewhere in the script.

The [[javascript/statements/return{{!}}return]] statement is used to return a value from the function. You do not have to use a return statement; the program will return when it reaches the end of the function. If no return statement is executed in the function, or if the return statement has no expression, the function returns the value undefined.

'''Note''' -- When you call a function, be sure to include the parentheses and any required arguments. Calling a function without parentheses returns a reference to the function, not the results of the function.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the function statement.

|Code= function myfunction (arg1, arg2) {
     var r = arg1 * arg2;
     return(r);
 }
}}{{Single_Example
|Language=JavaScript
|Description=A function can be assigned to a variable. This is illustrated in the following example.

|Code= function AddFive(x) {
     return x + 5;
 }
 
 function AddTen(x) {
     return x + 10;
 }
 
 var condition = false;
 
 var MyFunc;
 if (condition) {
     MyFunc = AddFive;
 }
 else {
     MyFunc = AddTen;
 }
 
 var result = MyFunc(123);
 // Output: 133
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/new{{!}}new Operator]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/4t2k5yhw(v=vs.94).aspx
|HTML5Rocks_link=
}}