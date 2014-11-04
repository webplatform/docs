{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
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
==Methods==
The following table lists methods of the '''Date Object'''.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Date/getDate|getDate]]
| Returns the day-of-the-month value using local time.
|-
| [[javascript/Date/getDay|getDay]]
| Returns the day-of-the-week value using local time.
|-
| [[javascript/Date/getFullYear|getFullYear]]
| Returns the year value using local time.
|-
| [[javascript/Date/getHours|getHours]]
| Returns the hours value using local time.
|-
| [[javascript/Date/getMilliseconds|getMilliseconds]]
| Returns the milliseconds value using local time.
|-
| [[javascript/Date/getMinutes|getMinutes]]
| Returns the minutes value using local time.
|-
| [[javascript/Date/getMonth|getMonth]]
| Returns the month value using local time.
|-
| [[javascript/Date/getSeconds|getSeconds]]
| Returns seconds value using local time.
|-
| [[javascript/Date/getTime|getTime]]
| Returns the time value in a Date Object as the number of milliseconds since midnight January 1, 1970.
|-
| [[javascript/Date/getTimezoneOffset|getTimezoneOffset]]
| Returns the difference in minutes between the time on the host computer and Universal Coordinated Time (UTC).
|-
| [[javascript/Date/getUTCDate|getUTCDate]]
| Returns the day-of-the-month value using UTC.
|-
| [[javascript/Date/getUTCDay|getUTCDay]]
| Returns the day-of-the-week value using UTC.
|-
| [[javascript/Date/getUTCFullYear|getUTCFullYear]]
| Returns the year value using UTC.
|-
| [[javascript/Date/getUTCHours|getUTCHours]]
| Returns the hours value using UTC.
|-
| [[javascript/Date/getUTCMilliseconds|getUTCMilliseconds]]
| Returns the milliseconds value using UTC.
|-
| [[javascript/Date/getUTCMinutes|getUTCMinutes]]
| Returns the minutes value using UTC.
|-
| [[javascript/Date/getUTCMonth|getUTCMonth]]
| Returns the month value using UTC.
|-
| [[javascript/Date/getUTCSeconds|getUTCSeconds]]
| Returns the seconds value using UTC.
|-
| [[javascript/Date/getYear|getYear]]
| Returns the year value .
|-
| [[javascript/Object/hasOwnProperty|hasOwnProperty]]
| Returns a Boolean value that indicates whether an object has a property with the specified name.
|-
| [[javascript/Object/isPrototypeOf|isPrototypeOf]]
| Returns a Boolean value that indicates whether an object exists in another object's prototype chain.
|-
| [[javascript/Object/propertyIsEnumerable|propertyIsEnumerable]]
| Returns a Boolean value that indicates whether a specified property is part of an object and whether it is enumerable.
|-
| [[javascript/Date/setDate|setDate]]
| Sets the numeric day of the month using local time.
|-
| [[javascript/Date/setFullYear|setFullYear]]
| Sets the year value using local time.
|-
| [[javascript/Date/setHours|setHours]]
| Sets the hours value using local time.
|-
| [[javascript/Date/setMilliseconds|setMilliseconds]]
| Sets the milliseconds value using local time.
|-
| [[javascript/Date/setMinutes|setMinutes]]
| Sets the minutes value using local time.
|-
| [[javascript/Date/setMonth|setMonth]]
| Sets the month value using local time.
|-
| [[javascript/Date/setSeconds|setSeconds]]
| Sets the seconds value using local time.
|-
| [[javascript/Date/setTime|setTime]]
| Sets the date and time value in the Date object.
|-
| [[javascript/Date/setUTCDate|setUTCDate]]
| Sets the numeric day of the month using UTC.
|-
| [[javascript/Date/setUTCFullYear|setUTCFullYear]]
| Sets the year value using UTC.
|-
| [[javascript/Date/setUTCHours|setUTCHours]]
| Sets the hours value using UTC.
|-
| [[javascript/Date/setUTCMilliseconds|setUTCMilliseconds]]
| Sets the milliseconds value using UTC.
|-
| [[javascript/Date/setUTCMinutes|setUTCMinutes]]
| Sets the minutes value using UTC.
|-
| [[javascript/Date/setUTCMonth|setUTCMonth]]
| Sets the month value using UTC.
|-
| [[javascript/Date/setUTCSeconds|setUTCSeconds]]
| Sets the seconds value using UTC.
|-
| [[javascript/Date/setYear|setYear]]
| Sets the year value using local time.
|-
| [[javascript/Date/toDateString|toDateString]]
| Returns a date as a string value.
|-
| [[javascript/Date/toGMTString|toGMTString]]
| Returns a date converted to a string using Greenwich Mean Time (GMT).
|-
| [[javascript/Date/toISOString|toISOString]]
| Returns a date as a string value in ISO format.
|-
| [[javascript/Date/toJSON|toJSON]]
| Used to transform data of an object type before the JSON serialization.
|-
| [[javascript/Date/toLocaleDateString|toLocaleDateString]]
| Returns a date as a string value appropriate to the host environment's current locale.
|-
| [[javascript/Object/toLocaleString|toLocaleString]]
| Returns an object converted to a string using the current locale.
|-
| [[javascript/Date/toLocaleTimeString|toLocaleTimeString]]
| Returns a time as a string value appropriate to the host environment's current locale.
|-
| [[javascript/Date/toString|toString]]
| Returns a string representation of an object.
|-
| [[javascript/Date/toTimeString|toTimeString]]
| Returns a time as a string value.
|-
| [[javascript/Date/toUTCString|toUTCString]]
| Returns a date converted to a string using UTC.
|-
| [[javascript/Date/valueOf|valueOf]]
| Returns the primitive value of the specified object.
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