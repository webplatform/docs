{{Page_Title}}
{{Flags}}
{{Summary_Section|Left shifts the bits of an expression.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''=''' expression1 '''&lt;&lt;''' expression2}}
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
|Remarks=The '''&lt;&lt;''' operator shifts the bits of expression1 left by the number of bits specified in expression2. For example:

 var temp
 temp = 14 &lt;&lt; 2
The variable temp has a value of 56 because 14 (00001110 in binary) shifted left two bits equals 56 (00111000 in binary).
}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/left shift assignment{{!}}Left Shift Assignment Operator (&#60;&#60;=)]]
* [[javascript/operators/bitwise right shift{{!}}Bitwise Right Shift Operator (&#62;&#62;)]]
* [[javascript/operators/unsigned right shift{{!}}Unsigned Right Shift Operator (&#62;&#62;&#62;)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/t7f48wx9(v=vs.94).aspx
|HTML5Rocks_link=
}}