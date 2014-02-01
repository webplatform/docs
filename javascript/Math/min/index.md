{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the smaller of a set of numeric expressions.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Math.min([ number1 [, number2 [... [, numberN ]]]])}}
}}
{{Remarks_Section
|Remarks=The optional number1, number2, ..., numberN arguments are numeric expressions to be evaluated.

If no arguments are provided, the return value is equal to [[javascript/Number/constants{{!}}Number.POSITIVE_INFINITY]]. If any argument is '''NaN''' , the return value is also '''NaN'''.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to get the smaller of two expressions.

|Code= var x = Math.min(107 - 3, 48 * 90);
 document.write(x);
 
 // Output:
 // 104
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Math/max{{!}}Math.max Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}