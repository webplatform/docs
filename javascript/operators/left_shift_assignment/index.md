{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Moves the specified number of bits to the left and assigns the result to result. The bits vacated by the operation are filled with 0.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result &lt;&lt;= expression
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression
|Description=The number of bits to move.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Using the '''&lt;&lt;=''' operator is the same as specifying <code>result = result &lt;&lt; expression</code>
|Code=// 14 is 00000000000000000000000000001110
var temp = 14;
temp &lt;&lt;= 2; 
document.write(temp);
// 56 is 00000000000000000000000000111000
Output: 56
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise left shift{{!}}Bitwise Left Shift Operator (&#60;&#60;)]]
* [[javascript/operators/bitwise right shift{{!}}Bitwise Right Shift Operator (&#62;&#62;)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/2027xe5w(v=vs.94).aspx
|HTML5Rocks_link=
}}