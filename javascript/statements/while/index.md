{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
}}
{{Summary_Section|Executes a statement or series of statements while a specified condition is true.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=while ( expression ) {
     statements
}
}}
|Values={{JS Syntax Parameter
|Name=expression
|Required=Required
|Description=A Boolean expression that is checked before each iteration of the loop. If expression is true, the loop is executed. If expression is false, the loop is terminated.
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
|Description=The following example illustrates the use of the while statement. The counter i increments until it reaches the value 100.
|Code=var i = 0;
while (i &lt; 100) {
    i++;
}
document.write(i);

//Output: 100
}}{{Single Example
|Language=JavaScript
|Description=In the following example an if statement has been placed within the while loop. Once the counter i has reached the value 10 the condition in the if statement becomes true and the loop is terminated.
|Code=var i = 0;
var j = 10;
while (i &lt; 100) {
    if (i === j) {
        break;
    }
    i++;
}
document.write(i);
 
// Output: 10
}}
}}
{{Remarks_Section
|Remarks=The while statement checks the expression before a loop is first executed. If expression is false at this time, the loop is never executed.
The while statement keeps iterating until the conditional expression returns false. It's essential that the expression can become false or that that loop is terminated with the break statement to prevent an infinite loop that will crash the program.
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