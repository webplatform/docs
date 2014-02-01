{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a date as a string value in ISO format.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= objDate.toISOString()}}
}}
{{JS_Return_Value
|Description=A string representation of the date in International Organization for Standardization (ISO) format.}}
==Exceptions==
If objDate does not contain a valid date, a RangeError exception is thrown.
{{Remarks_Section
|Remarks=The ISO format is a simplification of the ISO 8601 format. For more information, see Formatting Date and Time Strings (Windows Scripting - JScript).

The time zone is always UTC, denoted by the suffix Z in the output.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toISOString''' method.

|Code= var dt = new Date("30 July 2010 15:05 UTC");
 document.write(dt.toISOString());
 document.write("&lt;br /&gt;");
 document.write(dt.toUTCString());
 
 // Output:
 //  2010-07-30T15:05:00.000Z
 //  Fri, 30 Jul 2010 15:05:00 UTC
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date{{!}}Date Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff925953(v=vs.94).aspx
|HTML5Rocks_link=
}}