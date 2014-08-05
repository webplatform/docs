{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|The comma operator (''',''') causes two expressions to be executed sequentially.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=expression1 , expression2
}}
|Values={{JS Syntax Parameter
|Name=expression1
|Description=Any expression.
}}{{JS Syntax Parameter
|Name=expression2
|Description=Any expression.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The ''',''' operator causes the expressions to be executed in left-to-right order. A common use for the ''',''' operator is in the increment expression of a '''for''' loop. For example, the '''for''' statement allows only a single expression to be executed at the end of every pass through a loop. The ''',''' operator allows multiple expressions to be treated as a single expression, so both variables can be incremented.
|Code=j=25;
for (i = 0; i &lt; 10; i++, j++)
{
    k = i + j;
}
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/for{{!}}for Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9b37css7(v=vs.94).aspx
|HTML5Rocks_link=
}}