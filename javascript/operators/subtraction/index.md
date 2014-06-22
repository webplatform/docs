{{Page_Title}}
{{Flags
|State=Not Ready
|Checked_Out=No
}}
{{Summary_Section|Subtracts the value of one expression from another or provides unary negation of a single expression.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result '''=''' number1 '''-''' number2 ;
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any numeric variable.
}}{{JS Syntax Parameter
|Name=number1
|Description=Any numeric expression.
}}{{JS Syntax Parameter
|Name=number2
|Description=Any numeric expression.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=In Syntax 1, the '''-''' operator is the arithmetic subtraction operator used to find the difference between two numbers. In Syntax 2, the '''-''' operator is used as the unary negation operator to indicate the negative value of an expression.

For Syntax 2, as for all unary operators, expressions are evaluated as follows:

* If applied to undefined or null expressions, a run-time error is raised.
* Objects are converted to strings.
* Strings are converted to numbers if possible. If not, a run-time error is raised.
* Boolean values are treated as numbers (0 if false, 1 if true).
The operator is applied to the resulting number. In Syntax 2, if the resulting number is nonzero, result is equal to the resulting number with its sign reversed. If the resulting number is zero, result is zero.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/subtraction assignment{{!}}Subtraction Assignment Operator (-=)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9ty8kw3w(v=vs.94).aspx
|HTML5Rocks_link=
}}