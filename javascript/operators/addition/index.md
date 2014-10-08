{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
}}
{{Summary_Section|Adds the value of one numeric expression to another, or concatenates two strings.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result = expression1 '''+''' expression2
}}
|Values={{JS Syntax Parameter
|Name=result
|Required=
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression1
|Required=
|Description=Any expression.
}}{{JS Syntax Parameter
|Name=expression2
|Required=
|Description=Any expression.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=console.log(1 + 1); // 2
console.log("hello" + " world"); // "hello world"
console.log(1 + "1"); // "11"
console.log("1" + 1); // "11"
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The types of the two expressions determine the behavior of the '''+''' operator.

{{{!}} class='wikitable'
{{!}}-
! If
! Then
{{!}}-
{{!}} Both expressions are numeric or Boolean
{{!}} Add
{{!}}-
{{!}} Both expressions are strings
{{!}} Concatenate
{{!}}-
{{!}} One expression is numeric and the other is a string
{{!}} Concatenate
{{!}}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/addition assignment{{!}}Addition Assignment Operator (+=)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/wwfws59w(v=vs.94).aspx
|HTML5Rocks_link=
}}