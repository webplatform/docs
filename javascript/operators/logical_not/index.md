{{Page_Title}}
{{Flags
|State=Not Ready
|Checked_Out=No
}}
{{Summary_Section|Performs logical negation on an expression.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result '''= !''' expression
}}
|Values={{JS Syntax Parameter
|Name=result
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=expression
|Description=Any expression.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/zz722703(v=vs.94).aspx
|HTML5Rocks_link=
}}