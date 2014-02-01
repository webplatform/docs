{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the result of a bitwise AND operation on the value of a variable and the value of an expression. The variable and the expression are treated as 32-bit integers.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result &amp;= expression}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=expression
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=Using this operator is the same as specifying:

 result = result &amp; expression
The [[javascript/operators/bitwise and{{!}}Bitwise AND Operator (&amp;)]] looks at the binary representation of the values of result and expression and does a bitwise AND operation on them. The output of this operation behaves like this:

 // 9 is 00000000000000000000000000001001
 var expr1 = 9;
 
 // 5 is 00000000000000000000000000000101
 var expr2 = 5;
  
 
 // 1 is 00000000000000000000000000000001
 expr1 &amp;= expr2;
 
 document.write(expr1);
Any time both of the expressions have a 1 in a digit, the result has a 1 in that digit. Otherwise, the result has a 0 in that digit.
}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise and{{!}}Bitwise AND Operator (&#38;)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/a9h8y72a(v=vs.94).aspx
|HTML5Rocks_link=
}}