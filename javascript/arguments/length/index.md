{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the actual number of arguments passed to a function by the caller.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= [ function.] '''arguments'''.'''length'''}}
}}
{{Remarks_Section
|Remarks=The optional function argument is the name of the currently executing Function object.

The '''length''' property of the '''arguments''' object is initialized by the scripting engine to the actual number of arguments passed to a Function object when execution begins in that function.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''length''' property of the '''arguments''' object. To fully understand the example, pass more arguments to the function than the 2 arguments expected:

|Code= function ArgTest(a, b){
    var s = "";
 
    s += "Expected Arguments: " + ArgTest.length;
    s += "&lt;br /&gt;";
    s += "Passed Arguments: " + arguments.length;
 
    document.write (s);
 }
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7474tyd4(v=vs.94).aspx
|HTML5Rocks_link=
}}