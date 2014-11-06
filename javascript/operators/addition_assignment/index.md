{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Adds the value of an expression to the value of a variable and assigns the result to the variable.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result += expression
}}
|Values={{JS Syntax Parameter
|Name=result
|Required=
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression
|Required=
|Description=Any expression.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var x = 5;
x += 2;
// result: x = 7
|LiveURL=
}}
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
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/addition{{!}}Addition Operator (+)]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/w2xk8y0c(v=vs.94).aspx
|HTML5Rocks_link=
}}