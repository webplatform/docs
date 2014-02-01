{{Page_Title}}
{{Flags}}
{{Summary_Section|Converts a string to an integer.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= parseInt( numString , [ radix ]) }}
|Values={{JS_Syntax_Parameter
|Name=numString
|Required=Required
|Description=A string to convert into a number.}}{{JS_Syntax_Parameter
|Name=radix
|Required=Optional
|Description=A value between 2 and 36 that specifies the base of the number in numString. If this argument is not supplied, strings with a prefix of '0x' are considered hexadecimal. All other strings are considered decimal.}}
}}
{{Remarks_Section
|Remarks=The '''parseInt''' function returns an integer value equal to the number contained in numString. If no prefix of numString can be successfully parsed into an integer, '''NaN''' (not a number) is returned.

 parseInt("abc");     // Returns NaN.
 parseInt("12abc");   // Returns 12.
You can test for '''NaN''' using the '''isNaN''' function.
}}
{{See_Also_Section
|Manual_links=* [[javascript/isNaN{{!}}isNaN Function]]
* [[javascript/parseFloat{{!}}parseFloat Function]]
* [[javascript/String{{!}}String Object]]
* [[javascript/Object/valueOf{{!}}valueOf Method (Object)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/x53yedee(v=vs.94).aspx
|HTML5Rocks_link=
}}