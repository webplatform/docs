{{Page_Title}}
{{Flags
|State=Not Ready
|Checked_Out=No
}}
{{Summary_Section|Divides the value of one expression by the value of another, and returns the remainder.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result = number1 % number2
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any variable.
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
|Remarks=The modulus, or remainder, operator divides number1 by number2 and returns only the remainder as result. The sign of result is the same as the sign of number1. The value of result is between 0 and the absolute value of number2.

The following code shows how to use the modulus operator.

 var modResult = 19 % 6.7;
 document.write(modResult);
 
 // Output: 5.6
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9f59bza0(v=vs.94).aspx
|HTML5Rocks_link=
}}