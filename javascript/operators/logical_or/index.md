{{Page_Title}}
{{Flags}}
{{Summary_Section|Performs a logical disjunction on two expressions.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''=''' expression1 '''{{!}}{{!}}''' expression2}}
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
|Remarks=If either or both expressions evaluate to '''True''' , result is '''True'''. The following table illustrates how result is determined:

{{{!}} class='wikitable'
{{!}}-
! If <code>expression1</code> is
! And <code>expression2</code> is
! The <code>result</code> is
{{!}}-
{{!}} True
{{!}} True
{{!}} True
{{!}}-
{{!}} True
{{!}} False
{{!}} True
{{!}}-
{{!}} False
{{!}} True
{{!}} True
{{!}}-
{{!}} False
{{!}} False
{{!}} False
{{!}}} 
JavaScript uses the following rules for converting non-Boolean values to Boolean values:

* All objects are considered true.
* Strings are considered false if and only if they are empty.
* null and undefined are considered false.
* Numbers are false if, and only if, they are 0.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/xxxekd04(v=vs.94).aspx
|HTML5Rocks_link=
}}