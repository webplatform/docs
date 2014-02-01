{{Page_Title}}
{{Flags}}
{{Summary_Section|The increment operator increments, and the decrement operator decrements the value of a variable by one.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''=''' ++ variable }}{{JS_Syntax_Format
|Format= result = -- variable }}{{JS_Syntax_Format
|Format= result = variable ++}}{{JS_Syntax_Format
|Format= result = variable --}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=variable
|Required=
|Description=Any variable.}}
}}
{{Remarks_Section
|Remarks=If the operator appears before the variable, the value is modified before the expression is evaluated. If the operator appears after the variable, the value is modified after the expression is evaluated.  In other words, given <code>j = ++k;</code> , the value of <code>j</code> is the original value of <code>k</code> plus one; given <code>j = k++;</code> , the value of <code>j</code> is the original value of <code>k</code> , which is incremented after its value is assigned to <code>j</code>.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/26k41698(v=vs.94).aspx
|HTML5Rocks_link=
}}