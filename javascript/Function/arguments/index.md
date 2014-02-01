{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the arguments for the currently executing Function object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= function.arguments}}
}}
{{Remarks_Section
|Remarks=The function argument is the name of the currently executing function, and can be omitted.

This property allows a function to handle a variable number of arguments. The '''length''' property of the '''arguments''' object contains the number of arguments passed to the function. The individual arguments contained in the '''arguments''' object can be accessed in the same way array elements are accessed.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''arguments''' property:

|Code= function ArgTest(arg1, arg2){
    var s = "";
    s += "The individual arguments are: "
    for (n = 0; n &lt; arguments.length; n++){
       s += ArgTest.arguments[n];
       s += " ";
    }
    return(s);
 }
 document.write(ArgTest(1, 2, "hello"));
 
 //Output: function ArgTest(arg1, arg2){
    var s = "";
    s += "The individual arguments are: "
    for (n = 0; n &lt; arguments.length; n++){
       s += ArgTest.arguments[n];
       s += " ";
    }
    return(s);
 }
 document.write(ArgTest(1, 2, "hello"));
 
 // Output: The individual arguments are: 1 2 hello
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/arguments{{!}}arguments Object]]
* [[javascript/statements/function{{!}}function Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/he95z461(v=vs.94).aspx
|HTML5Rocks_link=
}}