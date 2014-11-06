{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Performs a bitwise OR on two expressions.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result '''=''' expression1 '''{{!}}''' expression2
}}
|Values={{JS Syntax Parameter
|Name=result
|Required=
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression1
|Required=
|Description=Any expression.
}}{{JS Syntax Parameter
|Name=expression2
|Required=
|Description=Any expression.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=See Remarks.
|Code=var x;
x = 5 {{!}} 12; 
// result: x = 13
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The '''{{!}}''' operator looks at the binary representation of the values of two expressions and does a bitwise OR operation on them. The result of this operation behaves as follows:

 0101   (expression1)
 1100   (expression2)
 ----
 1101   (result)
Any time either of the expressions has a 1 in a digit, the result will have a 1 in that digit. Otherwise, the result will have a 0 in that digit.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/bitwise or assignment{{!}}Bitwise OR Assignment Operator ({{!}}=)]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/066h456z(v=vs.94).aspx
|HTML5Rocks_link=
}}