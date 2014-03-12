{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|A number that is larger than the largest floating point number.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Infinity
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an initial value of '''Number.POSITIVE_INFINITY'''.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Divisions by zero will give you Infinity.
Divisions by negative zero will give you -Infinity.
|Code=42 / 0; // Infinity
42 / 0; // -Infinity
}}{{Single Example
|Language=JavaScript
|Description=Everything beyond Infinity remains Infinity
|Code=Infinity * Infinity; // Infinity
}}{{Single Example
|Language=JavaScript
|Description=If an arithmetic overflow occurs, Infinity is also returned
|Code=Math.pow(2, 1024); // Infinity
}}
}}
{{Remarks_Section
|Remarks=The '''Infinity''' constant is a member of the '''Global''' object, and is made available when the scripting engine is initialized.
}}
{{Notes_Section
|Notes===Negative Infinity==
Negative Infinity (-Infinity) is smaller than the smallest floating point number and returns a value of '''Number.NEGATIVE_INFINITY'''.

==Mathematical==
This value behaves mathematically like infinity; for example, anything multiplied by Infinity is Infinity, and anything divided by Infinity is 0.

Infinity subtracted by Infinity will return '''NaN'''

==isFinite()==
The [[javascript/isFinite{{!}}isFinite()]] function can be used to check if a given value is a finite number
}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Number/constants{{!}}Number Constants]]
* [[javascript/isFinite{{!}}isFinite()]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/kddt5x39(v=vs.94).aspx
|HTML5Rocks_link=
}}