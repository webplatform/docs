{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Gets the day of the week, using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getDay()
}}
|Values=
}}
{{JS_Return_Value
|Description=An integer between 0 and 6 representing the day of the week (Sunday is 0, Saturday is 6).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getDay''' method.
|Code=var date = new Date("Saturday, February 9, 2008");
 day = date.getDay();
 document.write(day);
 
 // Output: 6
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the day using Universal Coordinated Time (UTC), use the '''getUTCDay''' method.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCDay{{!}}getUTCDay Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/5wtd2bt8(v=vs.94).aspx
|HTML5Rocks_link=
}}