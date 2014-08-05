{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
}}
{{Summary_Section|The increment operator increments, and the decrement operator decrements, the value of a variable by one.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result '''=''' ++ variable
}}{{JS Syntax Format
|Format=result = -- variable
}}{{JS Syntax Format
|Format=result = variable ++
}}{{JS Syntax Format
|Format=result = variable --
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=variable
|Description=Any variable.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=If the operator appears before the variable, the value is modified before the expression is evaluated. If the operator appears after the variable, the value is modified after the expression is evaluated.  In other words, given <code>j = ++k;</code> , the value of <code>j</code> is the original value of <code>k</code> plus one; given <code>j = k++;</code> , the value of <code>j</code> is the original value of <code>k</code> , which is incremented after its value is assigned to <code>j</code>.
}}
{{Notes_Section}}
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/26k41698(v=vs.94).aspx
|HTML5Rocks_link=
}}