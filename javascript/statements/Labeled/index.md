{{Page_Title}}
{{Flags}}
{{Summary_Section|Provides an identifier for a statement.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= label ''':''' }}{{JS_Syntax_Format
|Format=     statements }}
|Values={{JS_Syntax_Parameter
|Name=label
|Required=Required
|Description=A unique identifier used when referring to the labeled statement.}}{{JS_Syntax_Parameter
|Name=statements
|Required=Optional
|Description=One or more statements associated with label.}}
}}
{{Remarks_Section
|Remarks=Labels are used by the '''break''' and '''continue''' statements to specify the statement to which the '''break''' and '''continue''' apply.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=In the following code, the '''continue''' statement refers to the '''for''' loop that is preceded by the <code>Inner:</code> statement. When <code>j</code> is 24, the '''continue''' statement causes that '''for''' loop to go to the next iteration. The numbers 21 through 23 and 25 through 30 print on each line.

|Code= Outer:
 for (i = 1; i &lt;= 10; i++) {
    document.write ("&lt;br /&gt;");
    document.write ("i: " + i);
    document.write (" j: ");
    
 Inner:
    for (j = 21; j &lt;= 30; j++) {
       if (j == 24)
           {
           continue Inner;
       }
       document.write (j + " ");
   }
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/break{{!}}break Statement]]
* [[javascript/statements/continue{{!}}continue Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/d3666y5k(v=vs.94).aspx
|HTML5Rocks_link=
}}