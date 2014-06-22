{{Page_Title}}
{{Flags
|State=Almost Ready
|Checked_Out=No
}}
{{Summary_Section|Terminates the current loop, or if in conjunction with a label , terminates the associated statement.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=break [ label ];
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In this example, the counter is set up to count from 1 to 99; however, the break statement terminates the loop after 14 counts.
|Code= for (var i = 1; i &lt; 100; i++) {
     if (i == 15) {
         break;
     }
     document.write (i);
     document.write (" ");
 }
 
 // Output: 1234567891011121314
}}{{Single Example
|Language=JavaScript
|Description=In the following code, the break statement refers to the for loop that is preceded by the <code>Inner:</code> statement. When <code>j</code> is equal to 24, the break statement causes the program flow to exit that loop. The numbers 21 through 23 print on each line.
|Code= Outer:
 for (var i = 1; i &lt;= 10; i++) {
     document.write ("&lt;br /&gt;");
     document.write ("i: " + i);
     document.write (" j: ");
 Inner:
     for (var j = 21; j &lt;= 30; j++) {
         if (j == 24) {
             break Inner;
         }
         document.write (j + " ");
     }
 }
 
 // Output: 
 // i: 1 j: 21 22 23 
 // i: 2 j: 21 22 23 
 // i: 3 j: 21 22 23 
 // i: 4 j: 21 22 23 
 // i: 5 j: 21 22 23 
 // i: 6 j: 21 22 23 
 // i: 7 j: 21 22 23 
 // i: 8 j: 21 22 23 
 // i: 9 j: 21 22 23 
 // i: 10 j: 21 22 23
}}
}}
{{Remarks_Section
|Remarks=The optional label argument specifies the label of the statement you are breaking from.

You typically use the break statement in switch statements and in while , for , for...in , or do...while loops. You most commonly use the label argument in switch statements, but it can be used in any statement, whether simple or compound.

Executing the break statement exits from the current loop or statement, and begins script execution with the statement immediately following.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/continue{{!}}continue Statement]]
* [[javascript/statements/do while{{!}}do...while Statement]]
* [[javascript/statements/for{{!}}for Statement]]
* [[javascript/statements/for in{{!}}for...in Statement]]
* [[javascript/statements/Labeled{{!}}Labeled Statement]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/3fhdxafb(v=vs.94).aspx
|HTML5Rocks_link=
}}