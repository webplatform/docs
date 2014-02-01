{{Page_Title}}
{{Flags}}
{{Summary_Section|Right shifts the value of a variable by the number of bits specified in the value of an expression, maintaining the sign, and assigns the result to the variable.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''&gt;&gt;=''' expression}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=expression
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=Using the '''&gt;&gt;=''' operator is exactly the same as specifying:

 result = result &gt;&gt; expression
The '''&gt;&gt;=''' operator shifts the bits of result right by the number of bits specified in expression. The sign bit of result is used to fill the digits from the left. Digits shifted off the right are discarded. For example, after the following code is evaluated, temp has a value of -4: 14 (11110010 in binary) shifted right two bits equals -4 (11111100 in binary).

 var temp
 temp = -14
 temp &gt;&gt;= 2
}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise left shift{{!}}Bitwise Left Shift Operator (&#60;&#60;)]]
* [[javascript/operators/bitwise right shift{{!}}Bitwise Right Shift Operator (&#62;&#62;)]]
* [[javascript/operators/unsigned right shift{{!}}Unsigned Right Shift Operator (&#62;&#62;&#62;)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7fd7s4a7(v=vs.94).aspx
|HTML5Rocks_link=
}}