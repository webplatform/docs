{{Page_Title}}
{{Flags}}
{{Summary_Section|Establishes the default object for a statement.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= with ( object ) {}}{{JS_Syntax_Format
|Format=     statements }}{{JS_Syntax_Format
|Format= } }}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=
|Description=The new default object.}}{{JS_Syntax_Parameter
|Name=statements
|Required=
|Description=One or more statements for which object is the default object.}}
}}
{{Remarks_Section
|Remarks=The with statement is commonly used to shorten the amount of code that you have to write in certain situations. In the example that follows, notice the repeated use of Math.

 x = Math.cos(3 * Math.PI) + Math.sin(Math.LN10) 
 y = Math.tan(14 * Math.E)
When you use the with statement, your code becomes shorter and easier to read:

 with (Math){
    x = cos(3 * PI) + sin (LN10)  
    y = tan(14 * E)
 }
}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/this{{!}}this Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/b294afx9(v=vs.94).aspx
|HTML5Rocks_link=
}}