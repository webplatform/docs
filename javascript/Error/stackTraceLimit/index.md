{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets or sets the stack trace limit, which is equivalent to the number of error frames to display. The default limit is 10.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Error '''.stackTraceLimit'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to set and then get the stack trace limit.
|Code=try
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
}}
}}
{{Remarks_Section
|Remarks=You can set the '''stackTraceLimit''' property to any positive value between 0 and Infinity. If the '''stackTraceLimit''' property is set to 0 at the time an error is thrown, no stack trace is shown. If the property is set to a negative value or a non-numeric value, the value is converted to 0. If the stackTraceLimit is set to Infinity , the entire stack is shown. Otherwise, ToUint32 is used to convert the value.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Error/description{{!}}description Property (Error)]]
* [[javascript/Error/message{{!}}message Property (Error)]]
* [[javascript/Error/name{{!}}name Property (Error)]]
* [[javascript/Error/stack{{!}}stack Property (Error)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh699849(v=vs.94).aspx
|HTML5Rocks_link=
}}