{{Page_Title}}
{{Flags}}
{{Summary_Section|Conditionally executes a group of statements, depending on the value of an expression.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= if ( condition1 ) {}}{{JS_Syntax_Format
|Format=     statement1 }}{{JS_Syntax_Format
|Format= }}}{{JS_Syntax_Format
|Format= [else if ( condition2 ) {}}{{JS_Syntax_Format
|Format=     statement2 }}{{JS_Syntax_Format
|Format= }]}}{{JS_Syntax_Format
|Format= [else {}}{{JS_Syntax_Format
|Format=     statement3 ] }}{{JS_Syntax_Format
|Format= }]}}
|Values={{JS_Syntax_Parameter
|Name=condition1
|Required=Required
|Description=A Boolean expression. If condition1 is null or undefined , condition1 is treated as false.}}{{JS_Syntax_Parameter
|Name=statement1
|Required=Optional
|Description=The statement to be executed if condition1 is '''true'''. Can be a compound statement.}}{{JS_Syntax_Parameter
|Name=condition2
|Required=
|Description=The condition to be evaluated.}}{{JS_Syntax_Parameter
|Name=statement2
|Required=Optional
|Description=The statement to be executed if condition2 is true. Can be a compound statement.}}{{JS_Syntax_Parameter
|Name=statement3
|Required=
|Description=If both condition1 and condition2 are false , this statement is executed.}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to use if , if else , and else.

It is good practice to enclose statement1 and statement2 in braces ({}) for clarity and to avoid inadvertent errors.

|Code= var z = 3;
 if (x == 5) {
     z = 10;
 }
 else if (x == 10) {
     z = 15;
 }
 else {
     z = 20;
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/conditional ternary{{!}}Conditional (Ternary) Operator (?:)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/85yyde5c(v=vs.94).aspx
|HTML5Rocks_link=
}}