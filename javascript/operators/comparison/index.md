{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns a Boolean value indicating the result of the comparison.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=expression1 comparisonoperator expression2
}}
|Values={{JS Syntax Parameter
|Name=expression1
|Required=
|Description=Any expression.
}}{{JS Syntax Parameter
|Name=comparisonoperator
|Required=
|Description=Any comparison operator (see Remarks).
}}{{JS Syntax Parameter
|Name=expression2
|Required=
|Description=Any expression.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=See Remarks.
|Code=var x = 5;
var y = 7;
var z = (x > y); // false
var z = (x < y); // true
var z = (y >= x); // true
var z = (y <= x); // false
|LiveURL=
}}
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
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ky6fyhws(v=vs.94).aspx
|HTML5Rocks_link=
}}