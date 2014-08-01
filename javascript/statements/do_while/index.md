{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
}}
{{Summary_Section|Executes a statement block once, and then repeats execution of the loop until a condition expression evaluates to false.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=do {
    statement
} while (expression) ;
}}
|Values={{JS Syntax Parameter
|Name=statement
|Required=Required
|Description=The statement to be executed if expression is true. Can be a compound statement.
}}{{JS Syntax Parameter
|Name=expression
|Required=Required
|Description=An expression that can be coerced to Boolean true or false. If expression is true , the loop is executed again. If expression is false , the loop is terminated.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In the following example, the statements in the do...while loop continue to execute as long as the variable <code>i</code> is less than 10.
|Code=var i = 0;
 do {
     document.write(i + " ");
     i++;
 } while (i &lt; 10);
 
 // Output: 0 1 2 3 4 5 6 7 8 9
}}{{Single Example
|Language=JavaScript
|Description=In the following example, the statements inside the loop are executed once even though the condition is not met.
|Code=var i = 10;
 do {
     document.write(i + " ");
     i++;
 } while (i &lt; 10);
 
 // Output: 10
}}
}}
{{Remarks_Section
|Remarks=Unlike the while statement, a do...while loop is executed one time before the conditional expression is evaluated.

On any line in a do...while block, you can use the break statement to cause the program flow to exit the loop, or you can use the continue statement to go directly to the while expression.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/break{{!}}break Statement]]
* [[javascript/statements/continue{{!}}continue Statement]]
* [[javascript/statements/for{{!}}for Statement]]
* [[javascript/statements/for in{{!}}for...in Statement]]
* [[javascript/statements/while{{!}}while Statement]]
* [[javascript/statements/Labeled{{!}}Labeled Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/5c1h7h0k(v=vs.94).aspx
|HTML5Rocks_link=
}}