{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Enables basic storage and retrieval of dates and times.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj = new Date()
}}{{JS Syntax Format
|Format=dateObj = new Date( dateVal )
}}{{JS Syntax Format
|Format=dateObj = new Date( year , month , date [, hours [, minutes [, seconds [, ms ]]]])
}}
|Values={{JS Syntax Parameter
|Name=dateObj
|Required=Required
|Description=The variable name to which the Date object is assigned.
}}{{JS Syntax Parameter
|Name=dateVal
|Required=Required
|Description=If a numeric value, dateVal represents the number of milliseconds in Universal Coordinated Time between the specified date and midnight January 1, 1970. If a string, dateVal is parsed according to the rules in Formatting Date and Time Strings (Windows Scripting - JScript). The dateVal argument can also be a VT_DATE value as returned from some ActiveX objects.
}}{{JS Syntax Parameter
|Name=year
|Required=Required
|Description=The full year, for example, 1976 (and not 76).
}}{{JS Syntax Parameter
|Name=month
|Required=Required
|Description=The month as an integer between 0 and 11 (January to December).
}}{{JS Syntax Parameter
|Name=date
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
|Description=The following example illustrates the use of the Date object.
|Code=var dateString = "Today's date is: ";
 
 var newDate = new Date();
 
 // Get the month, day, and year.
 dateString += (newDate.getMonth() + 1) + "/";
 dateString += newDate.getDate() + "/";
 dateString += newDate.getFullYear();
 
 document.write(dateString);
 
 // Output: Today's date is: &lt;date&gt;
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=A Date object contains a number representing a particular instant in time to within a millisecond. If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if you specify 150 seconds, JavaScript redefines that number as two minutes and 30 seconds.

If the number is '''NaN''' , the object does not represent a specific instant of time. If you pass no parameters to the Date object, it is initialized to the current time (UTC). A value must be given to the object before you can use it.

The range of dates that can be represented in a Date object is approximately 285,616 years on either side of January 1, 1970.

See Date and Time Calculations (Windows Scripting - JScript) for more information about how to use the Date object and related methods.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
==Properties==
The following table lists properties of the '''Date Object'''.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Date/constructor|constructor]]
| Specifies the function that creates an object.
|-
| [[javascript/Date/prototype|prototype]]
| Returns a reference to the prototype for a class of objects.
|}
==Functions==
The following table lists functions of the '''Date Object'''.

{| class='wikitable'
|-
! Functions
! Description
|-
| [[javascript/Date/now|Date.now]]
| Returns the number of milliseconds between January 1, 1970, and the current date and time.
|-
| [[javascript/Date/parse|Date.parse]]
| Parses a string containing a date, and returns the number of milliseconds between that date and midnight, January 1, 1970.
|-
| [[javascript/Date/UTC|Date.UTC]]
| Returns the number of milliseconds between midnight, January 1, 1970 Universal Coordinated Time (UTC) (or GMT) and the supplied date.
|}

{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Object
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/cd9w2te4(v=vs.94).aspx
|HTML5Rocks_link=
}}