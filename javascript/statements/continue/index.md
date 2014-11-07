{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Stops the current iteration of a loop, and starts a new iteration.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=continue [ label ];
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In this example, a loop iterates from 1 through 9. The statements between continue and the end of the for body are skipped because of the use of the continue statement together with the expression <code>(i &lt; 5)</code>.
|Code=for (var i = 1; i &lt; 10; i++) {
     if (i &lt; 5) {
         continue;
     }
     document.write (i);
     document.write (" ");
 }
 
 // Output: 5 6 7 8 9
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=In the following code, the continue statement refers to the for loop that is preceded by the <code>Inner:</code> label. When <code>j</code> is 24, the continue statement causes that for loop to go to the next iteration. The numbers 21 through 23 and 25 through 30 print on each line.
|Code=Outer:
 for (var i = 1; i &lt;= 10; i++) {
     document.write ("&lt;br /&gt;");
     document.write ("i: " + i);
     document.write (" j: ");
    
 Inner:
     for (var j = 21; j &lt;= 30; j++) {
         if (j == 24) {
              continue Inner;
         }
         document.write (j + " ");
     }
 }
 
 //Output:
 //i: 1 j: 21 22 23 25 26 27 28 29 30 
 //i: 2 j: 21 22 23 25 26 27 28 29 30 
 //i: 3 j: 21 22 23 25 26 27 28 29 30 
 //i: 4 j: 21 22 23 25 26 27 28 29 30 
 //i: 5 j: 21 22 23 25 26 27 28 29 30 
 //i: 6 j: 21 22 23 25 26 27 28 29 30 
 //i: 7 j: 21 22 23 25 26 27 28 29 30 
 //i: 8 j: 21 22 23 25 26 27 28 29 30 
 //i: 9 j: 21 22 23 25 26 27 28 29 30 
 //i: 10 j: 21 22 23 25 26 27 28 29 30
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The optional label argument specifies the statement to which continue applies.

You can use the continue statement only inside a while , do...while , '''for''' , or for...in loop. Executing the continue statement stops the current iteration of the loop and continues program flow with the beginning of the loop. This has the following effects on the different types of loops:

* while and do...while loops test their condition, and if true, execute the loop again.
* for loops execute their increment expression, and if the test expression is true, execute the loop again.
* for...in loops proceed to the next field of the specified variable and execute the loop again.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/break{{!}}break Statement]]
* [[javascript/statements/do while{{!}}do...while Statement]]
* [[javascript/statements/for{{!}}for Statement]]
* [[javascript/statements/for in{{!}}for...in Statement]]
* [[javascript/statements/Labeled{{!}}Labeled Statement]]
* [[javascript/statements/while{{!}}while Statement]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/8de3fkc8(v=vs.94).aspx
|HTML5Rocks_link=
}}