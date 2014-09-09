{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Gets the milliseconds of a Date, using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getMilliseconds()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns the milliseconds of a date. The value can range from 0-999. If a date has been constructed without specifying the milliseconds, the value returned is 0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getMilliseconds''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date.getMilliseconds());
 document.write("&lt;br/&gt;");
 
 date.setMilliseconds(5);
 document.write(date.getMilliseconds());
 // Output: 
 // 0
 // 5
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the number of milliseconds in Universal Coordinated Time (UTC), use the '''getUTCMilliseconds''' method.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCMilliseconds{{!}}getUTCMilliseconds Method (Date)]]
* [[javascript/Date/setMilliseconds{{!}}setMilliseconds Method (Date)]]
* [[javascript/Date/setUTCMilliseconds{{!}}setUTCMilliseconds Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/52s3k2tf(v=vs.94).aspx
|HTML5Rocks_link=
}}