{{Page_Title}}
{{Flags}}
{{Summary_Section|Adds the value of one numeric expression to another, or concatenates two strings.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result = expression1 '''+''' expression2}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=expression1
|Required=
|Description=Any expression.}}{{JS_Syntax_Parameter
|Name=expression2
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=The types of the two expressions determine the behavior of the '''+''' operator.

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
|Manual_links=* [[javascript/operators/addition assignment{{!}}Addition Assignment Operator (+=)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/wwfws59w(v=vs.94).aspx
|HTML5Rocks_link=
}}