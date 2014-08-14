{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the larger of a set of supplied numeric expressions.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Math.max([ number1 [, number2 [... [, numberN ]]]])
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to get the larger of two expressions.
|Code=var x = Math.max(107 - 3,  48 * 90);
 document.write(x);
 
 // Output:
 // 4320
}}
}}
{{Remarks_Section
|Remarks=The optional number1, number2, ..., numberN arguments are numeric expressions to be evaluated.

If no arguments are provided, the return value is equal to [[javascript/Number/constants{{!}}Number.NEGATIVE_INFINITY]]. If any argument is '''NaN''' , the return value is also '''NaN'''.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Math/min{{!}}Math.min Function]]
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