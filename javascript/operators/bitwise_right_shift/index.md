{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Right shifts the bits of an expression, maintaining sign.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result '''=''' expression1 '''&gt;&gt;''' expression2
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression1
|Description=Any expression.
}}{{JS Syntax Parameter
|Name=expression2
|Description=Any expression.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The &gt;&gt; operator shifts the bits of expression1 right by the number of bits specified in expression2. The sign bit of expression1 is used to fill the digits from the left. Digits shifted off the right are discarded. For example, after the following code is evaluated, temp has a value of -4: -14 (11110010 in two's complement binary) shifted right two bits equals -4 (11111100 in two's complement binary).
|Code=var temp
temp = -14 &gt;&gt; 2
}}
}}
{{Remarks_Section
|Remarks=
 
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise left shift{{!}}Bitwise Left Shift Operator (&#60;&#60;)]]
* [[javascript/operators/right shift assignment{{!}}Right Shift Assignment Operator (&#62;&#62;=)]]
* [[javascript/operators/unsigned right shift{{!}}Unsigned Right Shift Operator (&#62;&#62;&#62;)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/5s9e947e(v=vs.94).aspx
|HTML5Rocks_link=
}}