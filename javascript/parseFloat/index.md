{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Converts a string to a floating-point number.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=parseFloat( numString )
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
|Code=parseFloat("123.45") // returns 123.45
parseFloat("abc")      // returns NaN
parseFloat("1.2abc")   // returns 1.2

|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required numString argument is a string that contains a floating-point number.

The '''parseFloat''' function returns a numerical value equal to the number contained in numString. If no prefix of numString can be successfully parsed into a floating-point number, '''NaN''' (not a number) is returned.

You can test for '''NaN''' using the '''isNaN''' function.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/isNaN{{!}}isNaN Function]]
* [[javascript/parseInt{{!}}parseInt Function]]
* [[javascript/String{{!}}String Object]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/d5hbbd4z(v=vs.94).aspx
|HTML5Rocks_link=
}}