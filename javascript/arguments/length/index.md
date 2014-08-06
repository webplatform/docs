{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the actual number of arguments passed to a function by the caller.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=[ function.] '''arguments'''.'''length'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''length''' property of the '''arguments''' object. To fully understand the example, pass more arguments to the function than the 2 arguments expected:
|Code=function ArgTest(a, b){
    var s = "";
 
    s += "Expected Arguments: " + ArgTest.length;
    s += "&lt;br /&gt;";
    s += "Passed Arguments: " + arguments.length;
 
    document.write (s);
 }
}}
}}
{{Remarks_Section
|Remarks=The optional function argument is the name of the currently executing Function object.

The '''length''' property of the '''arguments''' object is initialized by the scripting engine to the actual number of arguments passed to a Function object when execution begins in that function.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Function/arguments{{!}}arguments Property (Function)]]
* [[javascript/Array/length{{!}}length Property (Array)]]
* [[javascript/String/length{{!}}length Property (String)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7474tyd4(v=vs.94).aspx
|HTML5Rocks_link=
}}