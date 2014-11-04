{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns the number of milliseconds between midnight, January 1, 1970 Universal Coordinated Time (UTC) (or GMT) and the specified date.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Date.UTC( year , month , day [ ''',''' hours [, minutes [, seconds [, ms ]]]])
}}
|Values={{JS Syntax Parameter
|Name=year
|Required=Required
|Description=The full year designation is required for cross-century date accuracy. If year is between 0 and 99 is used, then year is assumed to be 1900 + year.
}}{{JS Syntax Parameter
|Name=month
|Required=Required
|Description=The month as an integer between 0 and 11 (January to December).
}}{{JS Syntax Parameter
|Name=day
|Required=Required
|Description=The date as an integer between 1 and 31.
}}{{JS Syntax Parameter
|Name=hours
|Required=Optional
|Description=Must be supplied if minutes is supplied. An integer from 0 to 23 (midnight to 11pm) that specifies the hour.
}}{{JS Syntax Parameter
|Name=minutes
|Required=Optional
|Description=Must be supplied if seconds is supplied. An integer from 0 to 59 that specifies the minutes.
}}{{JS Syntax Parameter
|Name=seconds
|Required=Optional
|Description=Must be supplied if milliseconds is supplied. An integer from 0 to 59 that specifies the seconds.
}}{{JS Syntax Parameter
|Name=ms
|Required=Optional
|Description=An integer from 0 to 999 that specifies the milliseconds.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Date.UTC''' function.
|Code=// Determine the milliseconds per day.
  var MinMilli = 1000 * 60;
 var HrMilli = MinMilli * 60;
 var DyMilli = HrMilli * 24;
 
 var date = new Date("June 1, 1990");
 var year = date.getFullYear();
 var month = date.getMonth();
 var day = date.getDay();
 
 var newDay = new Date("January 16, 2020");
 var yeartoday = newDay.getUTCFullYear();
 var monthtoday = newDay.getUTCMonth();
 var dayofmonthtoday = newDay.getUTCDate();
  
 // Get the milliseconds since 1/1/1970 UTC.
 var t1 = Date.UTC(year, month - 1, day)
 var t2 = Date.UTC(yeartoday, monthtoday, dayofmonthtoday);
  
 // Determine the difference in days.
 var days = (t2 - t1) / DyMilli;
  
 document.write(days);
 // Output: 10848
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The '''Date.UTC''' function returns the number of milliseconds between midnight, January 1, 1970 UTC and the supplied date. This return value can be used in the '''setTime''' method and in the Date object constructor. If the value of an argument is greater than its range, or is a negative number, other stored values are modified accordingly. For example, if you specify 150 seconds, JavaScript redefines that number as two minutes and 30 seconds.

The difference between the '''Date.UTC''' function and the Date object constructor that accepts a date is that the '''Date.UTC''' function assumes UTC, and the Date object constructor assumes local time.
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
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/wz6stk2z(v=vs.94).aspx
|HTML5Rocks_link=
}}