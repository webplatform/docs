{{Page_Title}}
{{Flags}}
{{Summary_Section|Divides the value of one expression by the value of another, and returns the remainder.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result = number1 % number2}}
}}
==Arguments==
; result: Any variable.
; number1: Any numeric expression.
; number2: Any numeric expression.
{{Remarks_Section
|Remarks=The modulus, or remainder, operator divides number1 by number2 and returns only the remainder as result. The sign of result is the same as the sign of number1. The value of result is between 0 and the absolute value of number2.

The following code shows how to use the modulus operator.

 var modResult = 19 % 6.7;
 document.write(modResult);
 
 // Output: 5.6
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9f59bza0(v=vs.94).aspx
|HTML5Rocks_link=
}}