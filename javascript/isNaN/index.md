{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Determines whether a supplied number is [[javascript/NaN{{!}}NaN]] (not a number).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=isNaN(numValue)
}}
|Values={{JS Syntax Parameter
|Name=numValue
|Required=Required
|Description=the value to be tested against NaN
}}
}}
{{JS_Return_Value
|Description=true if the value, converted to the Number type, is the NaN; otherwise false.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=isNaN(100); // false
isNaN("100"); // false
isNaN("ABC"); // true
isNaN("10C"); // true
isNaN("abc123"); // true
isNaN(Math.sqrt(-1)); // true
}}
}}
{{Remarks_Section
|Remarks=You typically use this method to test return values from the [[javascript/parseInt{{!}}parseInt]] and [[javascript/parseFloat{{!}}parseFloat]] functions.

Alternatively, a variable that contains '''NaN''' or another value could be compared to itself. If it compares as unequal, it is '''NaN'''. This is because '''NaN''' is the only value that is not equal to itself.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/isFinite{{!}}isFinite Function]]
* [[javascript/NaN{{!}}NaN Constant]]
* [[javascript/parseFloat{{!}}parseFloat Function]]
* [[javascript/parseInt{{!}}parseInt Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/66ztdbe6(v=vs.94).aspx
|HTML5Rocks_link=
}}