{{Page_Title}}
{{Flags}}
{{Summary_Section|Performs logical negation on an expression.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result '''= !''' expression}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=expression
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=The following table illustrates how result is determined.

{{{!}} class='wikitable'
{{!}}-
! If <code>expression</code> is
! Then <code>result</code> is
{{!}}-
{{!}} True
{{!}} False
{{!}}-
{{!}} False
{{!}} True
{{!}}} 
All unary operators, such as the '''!''' operator, evaluate expressions as follows:

* If applied to undefined or null expressions, a run-time error is raised.
* Objects are converted to strings.
* Strings are converted to numbers if possible. If not, a run-time error is raised.
* Boolean values are treated as numbers (0 if false, 1 if true).
The operator is applied to the resulting number.

For the '''!''' operator, if expression is nonzero, result is zero. If expression is zero, result is 1.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/zz722703(v=vs.94).aspx
|HTML5Rocks_link=
}}