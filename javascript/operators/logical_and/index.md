{{Page_Title}}
{{Flags}}
{{Summary_Section|Performs a logical conjunction on two expressions.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result = expression1 &amp;&amp; expression2 }}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=expression1
|Required=
|Description=Any expression.}}{{JS_Syntax_Parameter
|Name=expression2
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=If both expressions evaluate to true , result is true. If either expression evaluates to false , result is false.

JavaScript uses the following rules for converting non-Boolean values to Boolean values:

* All objects are considered to be true.
* Strings are considered to be false if they are empty.
* null and undefined are considered to be false.
* A Number is false if it is zero.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/719e8e30(v=vs.94).aspx
|HTML5Rocks_link=
}}