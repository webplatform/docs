{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed import
|Checked_Out=No
}}
{{Summary_Section|Conditionally executes a group of statements, depending on the value of an expression.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=if ( condition1 ) {
     statement1
} else if ( condition2 ) {
     statement2
} else {
     statement3
}
}}
|Values={{JS Syntax Parameter
|Name=condition1
|Required=Required
|Description=A Boolean expression. If condition1 is null or undefined , condition1 is treated as false.
}}{{JS Syntax Parameter
|Name=statement1
|Required=Optional
|Description=The statement to be executed if condition1 is '''true'''. Can be a compound statement.
}}{{JS Syntax Parameter
|Name=condition2
|Description=The condition to be evaluated.
}}{{JS Syntax Parameter
|Name=statement2
|Required=Optional
|Description=The statement to be executed if condition2 is true. Can be a compound statement.
}}{{JS Syntax Parameter
|Name=statement3
|Description=If both condition1 and condition2 are false , this statement is executed.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to use if , if else , and else.

It is good practice to enclose statement1 and statement2 in braces ({}) for clarity and to avoid inadvertent errors.
|Code=var z = 3;
 if (x == 5) {
     z = 10;
 }
 else if (x == 10) {
     z = 15;
 }
 else {
     z = 20;
 }
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/conditional ternary{{!}}Conditional (Ternary) Operator (?:)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/85yyde5c(v=vs.94).aspx
|HTML5Rocks_link=
}}