{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns one of two expressions depending on a condition. Also referred to as "if...else shorthand".}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=test ? expression1 : expression2
}}
|Values={{JS Syntax Parameter
|Name=test
|Description=Any Boolean expression.
}}{{JS Syntax Parameter
|Name=expression1
|Description=An expression returned if test is true. May be a comma expression.
}}{{JS Syntax Parameter
|Name=expression2
|Description=An expression returned if test is false. More than one expression may be a linked by a comma expression.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The ?: operator can be used as a shortcut for an if...else statement. It is typically used as part of a larger expression where an if...else statement would be awkward. This example creates a string containing "Good evening." if it is after 6pm, or "Good day." otherwise.
|Code=var now = new Date();
var greeting = "Good" + ((now.getHours() &gt; 17) ? " evening." : " day.");
}}{{Single Example
|Language=JavaScript
|Description=The equivalent code using a regular if...else statement would look as follows:
|Code=var now = new Date();
var greeting = "Good";
if (now.getHours() &gt; 17)
    greeting += " evening.";
else
    greeting += " day.";
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/if else{{!}}if...else Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/be21c7hw(v=vs.94).aspx
|HTML5Rocks_link=
}}