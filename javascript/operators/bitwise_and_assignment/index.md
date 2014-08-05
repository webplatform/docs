{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Sets the result of a bitwise AND operation on the value of a variable and the value of an expression. The variable and the expression are treated as 32-bit integers.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result &amp;= expression
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression
|Description=Any expression.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Using this operator is the same as specifying <code>result = result &amp; expression</code>

The [[javascript/operators/bitwise and{{!}}Bitwise AND Operator (&amp;)]] looks at the binary representation of the values of result and expression and does a bitwise AND operation on them. The output of this operation behaves such that any time both of the expressions have a 1 in a digit, the result has a 1 in that digit; otherwise, the result has a 0 in that digit.
|Code=// 9 is 00000000000000000000000000001001
var expr1 = 9;
 
// 5 is 00000000000000000000000000000101
var expr2 = 5;
  
// 1 is 00000000000000000000000000000001
expr1 &amp;= expr2;
 
document.write(expr1);
// result: 1
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise and{{!}}Bitwise AND Operator (&#38;)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/a9h8y72a(v=vs.94).aspx
|HTML5Rocks_link=
}}