{{Page_Title}}
{{Flags}}
{{Summary_Section|Suspends execution.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= debugger}}
}}
{{Remarks_Section
|Remarks=You can place debugger statements anywhere in procedures to suspend execution. Using the debugger statement is similar to setting a breakpoint in the code.

The debugger statement suspends execution, but it does not close any files or clear any variables.

'''Note''' -- The debugger statement has no effect unless the script is being debugged.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=This example uses the debugger statement to suspend execution for each iteration through the for loop.

'''Note''' -- To run this example, you must have a script debugger installed and the script must run in debug mode.Internet Explorer 8 includes the JavaScript debugger. If you are using an earlier version of Internet Explorer, see [http://go.microsoft.com/fwlink/?LinkId=133801 How to: Enable and Start Script Debugging from Internet Explorer].

|Code= for(i = 1; i&lt;5; i++) {
    // Print i to the Output window.
    Debug.write("loop index is " + i);
    // Wait for user to resume.
    debugger
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/statements{{!}}JavaScript Statements]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/0bwt76sk(v=vs.94).aspx
|HTML5Rocks_link=
}}