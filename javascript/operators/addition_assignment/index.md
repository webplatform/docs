{{Page_Title}}
{{Flags}}
{{Summary_Section|Adds the value of an expression to the value of a variable and assigns the result to the variable.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result += expression }}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=expression
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=Using this operator is exactly the same as specifying: <code>result = result + expression</code>.

The types of the two expressions determine the behavior of the += operator.

{{{!}} class='wikitable'
{{!}}-
! If
! Then
{{!}}-
{{!}} Both expressions are numeric or Boolean
{{!}} Add
{{!}}-
{{!}} Both expressions are strings
{{!}} Concatenate
{{!}}-
{{!}} One expression is numeric and the other is a string
{{!}} Concatenate
{{!}}} 
}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/addition{{!}}Addition Operator (+)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/w2xk8y0c(v=vs.94).aspx
|HTML5Rocks_link=
}}