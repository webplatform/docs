{{Page_Title}}
{{Flags}}
{{Summary_Section|Causes two expressions to be executed sequentially.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= expression1 , expression2}}
|Values={{JS_Syntax_Parameter
|Name=expression1
|Required=
|Description=Any expression.}}{{JS_Syntax_Parameter
|Name=expression2
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=The ''',''' operator causes the expressions to be executed in left-to-right order. A common use for the ''',''' operator is in the increment expression of a '''for''' loop. For example:

 j=25;
 for (i = 0; i &lt; 10; i++, j++)
 {
    k = i + j;
 }
The '''for''' statement allows only a single expression to be executed at the end of every pass through a loop. The ''',''' operator allows multiple expressions to be treated as a single expression, so both variables can be incremented.
}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/for{{!}}for Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9b37css7(v=vs.94).aspx
|HTML5Rocks_link=
}}