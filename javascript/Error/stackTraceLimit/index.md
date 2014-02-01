{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets or sets the stack trace limit, which is equivalent to the number of error frames to display. The default limit is 10.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Error '''.stackTraceLimit''' }}
}}
{{Remarks_Section
|Remarks=You can set the '''stackTraceLimit''' property to any positive value between 0 and Infinity. If the '''stackTraceLimit''' property is set to 0 at the time an error is thrown, no stack trace is shown. If the property is set to a negative value or a non-numeric value, the value is converted to 0. If the stackTraceLimit is set to Infinity , the entire stack is shown. Otherwise, ToUint32 is used to convert the value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to set and then get the stack trace limit.

|Code= try
     {
     var err = new Error("my error");
     Error.stackTraceLimit = 7;
     throw err;
     }
 catch(e)
     {
     document.write ("Error stack trace limit: ")
     document.write (Error.stackTraceLimit);
     }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Error/description{{!}}description Property (Error)]]
* [[javascript/Error/message{{!}}message Property (Error)]]
* [[javascript/Error/name{{!}}name Property (Error)]]
* [[javascript/Error/stack{{!}}stack Property (Error)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh699849(v=vs.94).aspx
|HTML5Rocks_link=
}}