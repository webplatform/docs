{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a Boolean value that indicates whether a value is the reserved value '''NaN''' (not a number).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= isNaN( numValue ) }}
}}
{{JS_Return_Value
|Description=true if the value converted to the Number type is the NaN , otherwise false.}}
{{Remarks_Section
|Remarks=The required numValue is the value to be tested against '''NaN'''.

You typically use this method to test return values from the '''parseInt''' and '''parseFloat''' methods.

Alternatively, a variable that contains '''NaN''' or another value could be compared to itself. If it compares as unequal, it is '''NaN'''. This is because '''NaN''' is the only value that is not equal to itself.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Code= // Returns false.
 isNaN(100);
 
 // Returns false.
 isNaN("100");
 
 // Returns true.
 isNaN("ABC");
 
 // Returns true.
 isNaN("10C");
 
 // Returns true.
 isNaN("abc123");
 
 // Returns true.
 isNaN(Math.sqrt(-1));
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/isFinite{{!}}isFinite Function]]
* [[javascript/NaN{{!}}NaN Constant]]
* [[javascript/parseFloat{{!}}parseFloat Function]]
* [[javascript/parseInt{{!}}parseInt Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/66ztdbe6(v=vs.94).aspx
|HTML5Rocks_link=
}}