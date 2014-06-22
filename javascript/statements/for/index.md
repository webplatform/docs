{{Page_Title}}
{{Flags
|State=Not Ready
|Checked_Out=No
}}
{{Summary_Section|Executes a block of statements for as long as a specified condition is true.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=for ([ initialization ]; [ test ]; [ increment ]) {
    statement
}
}}
|Values={{JS Syntax Parameter
|Name=initialization
|Required=Optional
|Description=An expression. This expression is executed only once, before the loop is executed.
}}{{JS Syntax Parameter
|Name=test
|Required=Optional
|Description=A Boolean expression. If test is true , statement is executed. If test if false , the loop is terminated.
}}{{JS Syntax Parameter
|Name=increment
|Required=Optional
|Description=An expression. The increment expression is executed at the end of every pass through the loop.
}}{{JS Syntax Parameter
|Name=statement
|Required=Optional
|Description=One or more statements to be executed if test is '''true'''. Can be a compound statement.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In the following example, the for statement executes the enclosed statements as follows:

* First, the initial value of the variable <code>i</code> is evaluated.
* Then, as long as the value of <code>i</code> is less than or equal to 9, the <code>document.write</code> statements are executed and <code>i</code> is reevaluated.
* When <code>i</code> is greater than 9, the condition becomes false and control is transferred outside the loop.
|Code=// i is set to 0 at the start and is incremented by 1 at the
 // end of each iteration.
 // The loop terminates when i is not less than or equal to
 // 9 before a loop iteration.
 for (var i = 0; i &lt;= 9; i++) {
    document.write (i);
    document.write (" ");
 }
 
 // Output: 0 1 2 3 4 5 6 7 8 9
}}{{Single Example
|Language=JavaScript
|Description=All of the expressions of the for statement are optional. In the following example, the for statements create an infinite loop, and a break statement is used to exit the loop.
|Code=var j = 0;
 for (;;) {
     if (j &gt;= 5) {
         break;
     }
     j++;
     document.write (j + " ");
 }
 
 // Output: 1 2 3 4 5
}}
}}
{{Remarks_Section
|Remarks=You usually use a for loop when the loop is to be executed a known number of times. A for loop is useful for iterating over arrays and for performing sequential processing.

The test of a conditional expression occurs before the execution of the loop, so a for statement executes zero or more times.

On any line in a for loop statement block, you can use the break statement to exit the loop, or you can use the continue statement to transfer control to the next iteration of the loop.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/for in{{!}}for...in Statement]]
* [[javascript/statements/while{{!}}while Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/s1cyybdf(v=vs.94).aspx
|HTML5Rocks_link=
}}