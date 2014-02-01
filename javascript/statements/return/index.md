{{Page_Title}}
{{Flags}}
{{Summary_Section|Exits from the current function and returns a value from that function.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''return''' [ '''(''' ][ expression ][ ''')''' ]; }}
}}
{{Remarks_Section
|Remarks=The optional expression argument is the value to be returned from the function. If omitted, the function does not return a value.

You use the return statement to stop execution of a function and return the value of expression. If expression is omitted, or no return statement is executed from within the function, the expression that called the current function is assigned the value undefined.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the return statement.

|Code= function myfunction(arg1, arg2){
    var r;
    r = arg1 * arg2;
    return(r);
 }
}}{{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the return statement to return a function.

|Code= function doWork() {
     return function calculate(y) { return y + 1; };
 }
 
 var func = doWork();
 var x = func(5);
 document.write(x);
 
 // Output: 6
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/22a685h9(v=vs.94).aspx
|HTML5Rocks_link=
}}