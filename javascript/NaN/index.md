{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|A special constant that specifies a value that is Not-A-Number}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=NaN
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description='''NaN''' mainly occurs when parsing goes wrong
|Code=parseInt(123); // 123
parseInt("123"); // 123
parseInt('foo'); // NaN
}}{{Single Example
|Language=JavaScript
|Description='''NaN''' does not equal '''NaN''', use the [[javascript/isNaN{{!}}isNaN Function]] instead to test if a value is not a number
|Code=NaN === NaN; // false
isNaN(NaN); //true
}}
}}
{{Remarks_Section
|Remarks=The '''NaN''' constant is a member of the '''Global''' object, and is made available when the scripting engine is initialized.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/isNaN{{!}}isNaN Function]]
* [[javascript/Number{{!}}Number]]
* [[javascript/Number/constants{{!}}Number Constants]]
* [[javascript/parseInt{{!}}parseInt Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/z2bz9h52(v=vs.94).aspx
|HTML5Rocks_link=
}}