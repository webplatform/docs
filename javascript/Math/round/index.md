{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
}}
{{Summary_Section|Returns a supplied numeric expression rounded to the nearest integer.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''Math.round(''' number ''')'''
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=Math.round(0.8);  // 1
Math.round(2.2);  // 2
Math.round(2.5);  // 3
Math.round(4);    // 4
Math.round(-1.5); // -1
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required number argument is the value to be rounded to the nearest integer.

For positive numbers, if the decimal portion of number is 0.5 or greater, the return value is equal to the smallest integer greater than number. If the decimal portion is less than 0.5, the return value is the largest integer less than or equal to number.

For negative numbers, if the decimal portion is exactly -0.5, the return value is the smallest integer that is greater than the number.

For example, <code>Math.round(8.5)</code> returns 9, but <code>Math.round(-8.5)</code> returns -8.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Math/random{{!}}Math.random Function]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}