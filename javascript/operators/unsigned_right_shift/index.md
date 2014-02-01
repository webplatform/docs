{{Page_Title}}
{{Flags}}
{{Summary_Section|Right shifts the bits of an expression, without maintaining sign.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''=''' expression1 '''&gt;&gt;&gt;''' expression2}}
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
|Remarks=The '''&gt;&gt;&gt;''' operator shifts the bits of expression1 right by the number of bits specified in expression2. Zeroes are filled in from the left. Digits shifted off the right are discarded. For example:

 var temp
 temp = -14 &gt;&gt;&gt; 2
The variable temp has an initial value -14 (11111111 11111111 11111111 11110010 in two's complement binary). When it is shifted right two bits, the value equals 1073741820 (00111111 11111111 11111111 11111100 in binary).
}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/unsigned right shift assignment{{!}}Unsigned Right Shift Assignment Operator (&#62;&#62;&#62;=)]]
* [[javascript/operators/bitwise left shift{{!}}Bitwise Left Shift Operator (&#60;&#60;)]]
* [[javascript/operators/bitwise right shift{{!}}Bitwise Right Shift Operator (&#62;&#62;)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/342xfs5s(v=vs.94).aspx
|HTML5Rocks_link=
}}