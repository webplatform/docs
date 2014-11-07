{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Exits from the current function and returns a value from that function.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''return''' [ '''(''' ][ expression ][ ''')''' ];
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the return statement.
|Code=function myfunction(arg1, arg2){
    var r;
    r = arg1 * arg2;
    return(r);
 }
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the return statement to return a function.
|Code=function doWork() {
     return function calculate(y) { return y + 1; };
 }
 
 var func = doWork();
 var x = func(5);
 document.write(x);
 
 // Output: 6
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The optional expression argument is the value to be returned from the function. If omitted, the function does not return a value.

You use the return statement to stop execution of a function and return the value of expression. If expression is omitted, or no return statement is executed from within the function, the expression that called the current function is assigned the value undefined.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/22a685h9(v=vs.94).aspx
|HTML5Rocks_link=
}}