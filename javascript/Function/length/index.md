{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the number of arguments defined for a function.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= functionName.length}}
}}
{{Remarks_Section
|Remarks=The required functionName is the name of the function.

The '''length''' property of a function is initialized by the scripting engine to the number of arguments in the function's definition when an instance of the function is created.

What happens when a function is called with a number of arguments different from the value of its '''length''' property depends on the function.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''length''' property:

|Code= function ArgTest(a, b){
     var s = "";
 
     s += "Expected Arguments: " + ArgTest.length;
     s += "&lt;br /&gt;";
     s += "Passed Arguments: " + arguments.length;
 
     return s;
 }
 
 document.write(ArgTest(1, 2));
 
 // Output: 
 // Expected Arguments: 2
 // Passed Arguments: 2
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Function/arguments{{!}}arguments Property (Function)]]
* [[javascript/Array/length{{!}}length Property (Array)]]
* [[javascript/String/length{{!}}length Property (String)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/4cz6db7d(v=vs.94).aspx
|HTML5Rocks_link=
}}