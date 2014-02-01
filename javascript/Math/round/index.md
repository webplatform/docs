{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a supplied numeric expression rounded to the nearest integer.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''Math.round(''' number ''')''' }}
}}
{{Remarks_Section
|Remarks=The required number argument is the value to be rounded to the nearest integer.

For positive numbers, if the decimal portion of number is 0.5 or greater, the return value is equal to the smallest integer greater than number. If the decimal portion is less than 0.5, the return value is the largest integer less than or equal to number.

For negative numbers, if the decimal portion is exactly -0.5, the return value is the smallest integer that is greater than the number.

For example, <code>Math.round(8.5)</code> returns 9, but <code>Math.round(-8.5)</code> returns -8.
}}
{{See_Also_Section
|Manual_links=* [[javascript/Math/random{{!}}Math.random Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}