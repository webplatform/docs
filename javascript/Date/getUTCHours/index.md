{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Gets the hours value in a '''Date''' object using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getUTCHours()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an integer between 0 and 23 indicating the number of hours since midnight. Zero is returned if the time is before 1:00:00 am. If a '''Date''' object was created without specifying the time, by default the hour is 0 in UTC time. This time may be non-zero in other time zones.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getUTCHours''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date.getUTCHours());
 document.write("&lt;br/&gt;");
 
 var date2 = new Date("1/1/2001 11:22:33");
 document.write(datee.getUTCHours());
 
 // Output (in the PST time zone):
 // 8
 // 19
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the number of hours elapsed since midnight using local time, use the '''getHours''' method.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getHours{{!}}getHours Method (Date)]]
* [[javascript/Date/setHours{{!}}setHours Method (Date)]]
* [[javascript/Date/setUTCHours{{!}}setUTCHours Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/s12ec8ba(v=vs.94).aspx
|HTML5Rocks_link=
}}