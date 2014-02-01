{{Page_Title}}
{{Flags}}
{{Summary_Section|Performs a bitwise OR on two expressions.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''=''' expression1 '''{{!}}''' expression2}}
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
|Remarks=The '''{{!}}''' operator looks at the binary representation of the values of two expressions and does a bitwise OR operation on them. The result of this operation behaves as follows:

 0101   (expression1)
 1100   (expression2)
 ----
 1101   (result)
Any time either of the expressions has a 1 in a digit, the result will have a 1 in that digit. Otherwise, the result will have a 0 in that digit.
}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise or assignment{{!}}Bitwise OR Assignment Operator ({{!}}=)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/066h456z(v=vs.94).aspx
|HTML5Rocks_link=
}}