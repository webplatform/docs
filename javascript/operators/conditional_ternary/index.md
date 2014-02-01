{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns one of two expressions depending on a condition.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= test ? expression1 : expression2}}
|Values={{JS_Syntax_Parameter
|Name=test
|Required=
|Description=Any Boolean expression.}}{{JS_Syntax_Parameter
|Name=expression1
|Required=
|Description=An expression returned if test is true. May be a comma expression.}}{{JS_Syntax_Parameter
|Name=expression2
|Required=
|Description=An expression returned if test is false. More than one expression may be a linked by a comma expression.}}
}}
{{Remarks_Section
|Remarks=The ?: operator can be used as a shortcut for an if...else statement. It is typically used as part of a larger expression where an if...else statement would be awkward. For example:

 var now = new Date();
 var greeting = "Good" + ((now.getHours() &gt; 17) ? " evening." : " day.");
The example creates a string containing "Good evening." if it is after 6pm. The equivalent code using an if...else statement would look as follows:

 var now = new Date();
 var greeting = "Good";
 if (now.getHours() &gt; 17)
    greeting += " evening.";
 else
    greeting += " day.";
}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/if else{{!}}if...else Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/be21c7hw(v=vs.94).aspx
|HTML5Rocks_link=
}}