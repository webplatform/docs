{{Page_Title}}
{{Flags}}
{{Summary_Section|Converts a string to a floating-point number.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= parseFloat( numString ) }}
}}
{{Remarks_Section
|Remarks=The required numString argument is a string that contains a floating-point number.

The '''parseFloat''' function returns a numerical value equal to the number contained in numString. If no prefix of numString can be successfully parsed into a floating-point number, '''NaN''' (not a number) is returned.

 parseFloat("abc")      // Returns NaN.
 parseFloat("1.2abc")   // Returns 1.2.
You can test for '''NaN''' using the '''isNaN''' function.
}}
{{See_Also_Section
|Manual_links=* [[javascript/isNaN{{!}}isNaN Function]]
* [[javascript/parseInt{{!}}parseInt Function]]
* [[javascript/String{{!}}String Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/d5hbbd4z(v=vs.94).aspx
|HTML5Rocks_link=
}}