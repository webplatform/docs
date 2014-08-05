{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
}}
{{Summary_Section|Performs a logical conjunction on two expressions.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result = expression1 &amp;&amp; expression2
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression1
|Description=Any expression.
}}{{JS Syntax Parameter
|Name=expression2
|Description=Any expression.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=If both expressions evaluate to true, result is true. If either expression evaluates to false, result is false.

JavaScript uses the following rules for converting non-Boolean values to Boolean values:

* All objects are considered to be true.
* Strings are considered to be false if they are empty.
* null and undefined are considered to be false.
* A Number is false if it is zero.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/719e8e30(v=vs.94).aspx
|HTML5Rocks_link=
}}