{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Performs a bitwise AND operation on two 32-bit expressions.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result = expression1 &amp; expression2
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=The result of the operation.
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
|Description=The following examples show how to use the &amp; operator. See Remarks for more information.
|Code=// 9 is 00000000000000000000000000001001
var expr1 = 9;
 
// 5 is 00000000000000000000000000000101
var expr2 = 5;
 
// 1 is 00000000000000000000000000000001
var result = expr1 &amp; expr2;
 
document.write(result);
// Output: 1
}}
}}
{{Remarks_Section
|Remarks=The &amp; does a bitwise AND operation on the each of the bits of two 32-bit expressions. If both of the bits are 1, the result is 1. Otherwise, the result is 0.

{{{!}} class='wikitable'
{{!}}-
! Bit1
! Bit2
! ANDed Value
{{!}}-
{{!}} 0
{{!}} 0
{{!}} 0
{{!}}-
{{!}} 1
{{!}} 1
{{!}} 1
{{!}}-
{{!}} 1
{{!}} 0
{{!}} 0
{{!}}-
{{!}} 0
{{!}} 1
{{!}} 0
{{!}}} 


}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise and assignment{{!}}Bitwise AND Assignment Operator (&#38;=)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dazfy1f3(v=vs.94).aspx
|HTML5Rocks_link=
}}