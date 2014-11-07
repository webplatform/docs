{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
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
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var i = 0;

while (i < 5) {
  console.log("This runs 5 times");
  i++;
}
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=
|Code=var i = 0;

while (i < 100) {
  if (i == 5) {
    // Stop the while loop early
    break;
  }
  console.log("This happens 5 times");
  i++;
}
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=The while statement checks the expression before a loop is first executed. If expression is false at this time, the loop is never executed.

The while statement keeps iterating until the conditional expression returns false, or encounters a break statement.

It's essential that the expression can become false or that that loop is terminated with the break statement to prevent an infinite loop.
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/break{{!}}break Statement]]
* [[javascript/statements/continue{{!}}continue Statement]]
* [[javascript/statements/do while{{!}}do...while Statement]]
* [[javascript/statements/for{{!}}for Statement]]
* [[javascript/statements/for in{{!}}for...in Statement]]
|External_links=
|Manual_sections==== Specification ===

* [http://www.ecma-international.org/ecma-262/5.1/#sec-12.6.2 ECMAScript 5.1 (ECMA-262) - The while statement]
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