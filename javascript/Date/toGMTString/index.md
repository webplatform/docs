{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns a date converted to a string using Greenwich Mean Time(GMT).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''toGMTString()'''
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var date = new Date("2014-05-09");
console.log(date.toGMTString()); // "Fri, 09 May 2014 00:00:00 GMT"
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is any Date object.

The '''toGMTString''' method is obsolete, and is provided for backwards compatibility only. It is recommended that you use the '''toUTCString''' method instead.

The '''toGMTString''' method returns a String object that contains the date formatted using GMT convention. The format of the return value is as follows: "05 Jan 1996 00:00:00 GMT."
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toUTCString{{!}}toUTCString Method (Date)]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Date
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/a34ehb82(v=vs.94).aspx
|HTML5Rocks_link=
}}