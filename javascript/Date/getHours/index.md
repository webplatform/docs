{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the hours in a date, using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getHours()
}}
|Values=
}}
{{JS_Return_Value
|Description=An integer between 0 and 23, indicating the number of hours since midnight. Zero is returned if the time is before 1:00:00 am. If a '''Date''' object was created without specifying the time, by default the hour is 0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getHours''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date.getHours());
 document.write("&lt;br/&gt;");
 
 date.setTime(50000000);
 document.write(date.getHours());
 
 // Output:
 // 0 
 // 5
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the hours value using Universal Coordinated Time (UTC), use the '''getUTCHours''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCHours{{!}}getUTCHours Method (Date)]]
* [[javascript/Date/setHours{{!}}setHours Method (Date)]]
* [[javascript/Date/setUTCHours{{!}}setUTCHours Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/815z9tc9(v=vs.94).aspx
|HTML5Rocks_link=
}}