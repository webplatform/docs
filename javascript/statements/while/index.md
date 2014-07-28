{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed import
|Checked_Out=Yes
}}
{{Summary_Section|Executes a statement or series of statements until a specified condition is false.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=while ( expression ) {
     statements
}
}}
|Values={{JS Syntax Parameter
|Name=expression
|Required=Required
|Description=A Boolean expression that is checked before each iteration of the loop. If expression is true , the loop is executed. If expression is false , the loop is terminated.
}}{{JS Syntax Parameter
|Name=statements
|Required=Optional
|Description=One or more statements to be executed if expression is true.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the while statement.
|Code=var i = 0;
 var j = 10;
 while (i &lt; 100) {
     if (i == j)
         break;
     i++;
 }
 document.write(i);
 
 // Output: 10
}}
}}
{{Remarks_Section
|Remarks=The while statement checks expression before a loop is first executed. If expression is false at this time, the loop is never executed.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/break{{!}}break Statement]]
* [[javascript/statements/continue{{!}}continue Statement]]
* [[javascript/statements/do while{{!}}do...while Statement]]
* [[javascript/statements/for{{!}}for Statement]]
* [[javascript/statements/for in{{!}}for...in Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/6wsy66x9(v=vs.94).aspx
|HTML5Rocks_link=
}}