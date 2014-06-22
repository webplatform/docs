{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed import
|Checked_Out=No
}}
{{Summary_Section|Establishes the default object for a statement.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=with ( object ) {
     statements
}
}}
|Values={{JS Syntax Parameter
|Name=object
|Description=The new default object.
}}{{JS Syntax Parameter
|Name=statements
|Description=One or more statements for which object is the default object.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
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
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/this{{!}}this Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/b294afx9(v=vs.94).aspx
|HTML5Rocks_link=
}}