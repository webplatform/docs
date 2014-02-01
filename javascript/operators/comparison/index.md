{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a Boolean value indicating the result of the comparison.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= expression1 comparisonoperator expression2}}
|Values={{JS_Syntax_Parameter
|Name=expression1
|Required=
|Description=Any expression.}}{{JS_Syntax_Parameter
|Name=comparisonoperator
|Required=
|Description=Any comparison operator.}}{{JS_Syntax_Parameter
|Name=expression2
|Required=
|Description=Any expression.}}
}}
{{Remarks_Section
|Remarks=When comparing strings, JavaScript uses the Unicode character value of the string expression.

The following describes how the different groups of operators behave depending on the types and values of expression1 and expression2 :

Relational operators: '''&lt;''' , '''&gt;''' , '''&lt;=''' , '''&gt;='''

* Attempt to convert both expression1 and expression2 into numbers.
* If both expressions are strings, do a string comparison.
* If either expression is '''NaN''' , return false.
* Negative zero equals Positive zero.
* Negative Infinity is less than everything including itself.
* Positive Infinity is greater than everything including itself.
Equality operators: '''==''' , '''!='''

* If the types of the two expressions are different, attempt to convert them to a String, Number, or Boolean.
* '''NaN''' is not equal to anything including itself.
* Negative zero equals positive zero.
* null equals both null and undefined.
* Values are considered equal if they are identical strings, numerically equivalent numbers, the same object, identical Boolean values, or (if different types) they can be coerced into one of these situations.
* Every other comparison is considered unequal.
Identity operators: '''===''' , '''!=='''

These operators behave the same as the equality operators, except that no type conversion is done. If the types of both expressions are not the same, these expressions always return false.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ky6fyhws(v=vs.94).aspx
|HTML5Rocks_link=
}}