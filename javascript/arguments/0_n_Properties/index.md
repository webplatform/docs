{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the actual value of individual arguments from an '''arguments''' object returned by the '''arguments''' property of an executing function.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= [ function '''.''' ] '''arguments[''' [0{{!}}1{{!}}2{{!}}...{{!}} n ] ''']'''}}
|Values={{JS_Syntax_Parameter
|Name=function
|Required=Optional
|Description=The name of the currently executing Function object.}}{{JS_Syntax_Parameter
|Name=0, 1, 2, , n
|Required=Required
|Description=Non-negative integer in the range of 0 to n where 0 represents the first argument and n represents the final argument. The value of the final argument n is '''arguments.length-1'''.}}
}}
{{Remarks_Section
|Remarks=The values returned by the 0 . . . n properties are the actual values passed to the executing function. While not actually an array of arguments, the individual arguments that comprise the '''arguments''' object are accessed the same way that array elements are accessed.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''0 . . .''' n properties of the '''arguments''' object. To fully understand the example, pass one or more arguments to the function:

|Code= function ArgTest(){
    var s = "";
    s += "The individual arguments are: "
    for (n = 0; n &lt; arguments.length; n++){
       s += ArgTest.arguments[n] ;
       s += " ";
    }
    return(s);
 }
 document.write(ArgTest(1, 2, "hello", new Date()));
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/arguments/length{{!}}length Property (arguments)]]
* [[javascript/Function/length{{!}}length Property (Function)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/bb79e676(v=vs.94).aspx
|HTML5Rocks_link=
}}