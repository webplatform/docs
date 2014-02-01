{{Page_Title}}
{{Flags}}
{{Summary_Section|Performs a bitwise NOT (negation) on an expression.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''=''' '''~''' expression}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=expression
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=All unary operators, such as the ~ operator, evaluate expressions as follows:

* If applied to undefined or null expressions, a run-time error is raised.
* Objects are converted to strings.
* Strings are converted to numbers if possible. If not, a run-time error is raised.
* Boolean values are treated as numbers (0 if false, 1 if true).
The operator is applied to the resulting number.

The ~ operator looks at the binary representation of the values of the expression and does a bitwise negation operation on it.

Any digit that is a 1 in the expression becomes a 0 in the result. Any digit that is a 0 in the expression becomes a 1 in the result.

The following example illustrates use of the bitwise NOT (~) operator.

 var temp = ~5;
The resulting value is -6, as shown in the following table.

{{{!}} class='wikitable'
{{!}}-
! Expression
! Binary value (two's complement)
! Decimal value
{{!}}-
{{!}} 5
{{!}} 00000000 00000000 00000000 00000101
{{!}} 5
{{!}}-
{{!}} ~5
{{!}} 11111111 11111111 11111111 11111010
{{!}} -6
{{!}}} 
}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/logical not{{!}}Logical NOT Operator (!)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/zf9s465t(v=vs.94).aspx
|HTML5Rocks_link=
}}