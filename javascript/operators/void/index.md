{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|The void operator evaluates an expression but then returns <b>undefined</b>.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=void expression
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=The expression argument is any valid JavaScript expression.

The void operator evaluates its expression and returns undefined. It is useful in situations where an expression should be evaluated but you do not want the results visible to the rest of the script.

It is important to note that void works only on unary expressions thus: <code> void x, y; </code>
will set only the x variable to <b>undefined</b>.
}}
{{Notes_Section
|Notes=void(0) is equivalent to void 0 and returns the <b>undefined</b> value
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/e17c7cbe(v=vs.94).aspx
|HTML5Rocks_link=
}}