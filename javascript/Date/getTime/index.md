{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Gets the time value in milliseconds.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getTime()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns the number of milliseconds between midnight, January 1, 1970 and the time value in the Date object. The range of dates is approximately 285,616 years from either side of midnight, January 1, 1970. Negative numbers indicate dates prior to 1970.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getTime''' method.
|Code=var minute = 1000 * 60;
 var hour = minute * 60;
 var day = hour * 24;
 
 date = new Date("1/1/2001");
 var time = date.getTime();
 
 document.write(Math.round(time / day) + " days from 1/1/1970 to 1/1/2001");
 
 // Output: 11323 days from 1/1/1970 to 1/1/2001
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. 

When doing multiple date and time calculations, you may want to define variables equal to the number of milliseconds in a day, hour, or minute. For example:

 var minute = 1000 * 60;
 var hour = minute * 60;
 var day = hour * 24;

See Date and Time Calculations (Windows Scripting - JScript) for more information about how to use the '''getTime''' method.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/setTime{{!}}setTime Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7hcawkw2(v=vs.94).aspx
|HTML5Rocks_link=
}}