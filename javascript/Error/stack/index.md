{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets or sets the error stack as a string that contains the stack trace frames.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= object '''.stack''' }}
}}
{{Remarks_Section
|Remarks=The '''stack''' property is set to undefined when the error is constructed, and gets the trace information when the error is raised. If an error is raised multiple times, the '''stack''' property is updated each time the error is raised.

Stack frames are displayed in the following format: at FunctionName (&lt;Fully-qualified name/URL&gt;:&lt;line number&gt;:&lt;column number&gt;)

If you create your own Error object and set the stack trace to a value, the value won't be overwritten when the error is thrown.

The '''stack''' property does not show inline functions in its frames. It shows only the physical stack.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the stack when you're catching an error.

|Code= try
     {
         var x = y.name;
     }
 catch(e)
     {
         document.write ("Error stack: ")
         document.write (e.stack);
     }
}}{{Single_Example
|Language=JavaScript
|Description=The following example shows how to set and then get the stack.

|Code= try
     {
         var err = Error("my error");
         err.stack = "my stack trace";
         throw err;
     }
 catch(e)
     {
         document.write ("Error stack: ")
         document.write (e.stack);
     }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Error/description{{!}}description Property (Error)]]
* [[javascript/Error/message{{!}}message Property (Error)]]
* [[javascript/Error/name{{!}}name Property (Error)]]
* [[javascript/Error/stackTraceLimit{{!}}stackTraceLimit Property (Error)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh699850(v=vs.94).aspx
|HTML5Rocks_link=
}}