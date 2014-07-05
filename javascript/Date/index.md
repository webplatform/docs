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
{{JS_Return_Value}}
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
}}
}}
{{Remarks_Section
|Remarks=A Date object contains a number representing a particular instant in time to within a millisecond. If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if you specify 150 seconds, JavaScript redefines that number as two minutes and 30 seconds.

If the number is '''NaN''' , the object does not represent a specific instant of time. If you pass no parameters to the Date object, it is initialized to the current time (UTC). A value must be given to the object before you can use it.

The range of dates that can be represented in a Date object is approximately 285,616 years on either side of January 1, 1970.

See Date and Time Calculations (Windows Scripting - JScript) for more information about how to use the Date object and related methods.
}}
{{Notes_Section}}
{{JS Object Listing}}
==Properties==
The following table lists properties of the '''Date Object'''.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Date/constructor|constructor Property]]
| Specifies the function that creates an object.
|-
| [[javascript/Date/prototype|prototype Property]]
| Returns a reference to the prototype for a class of objects.
|}
==Functions==
The following table lists functions of the '''Date Object'''.

{| class='wikitable'
|-
! Functions
! Description
|-
| [[javascript/Date/now|Date.now Function]]
| Returns the number of milliseconds between January 1, 1970, and the current date and time.
|-
| [[javascript/Date/parse|Date.parse Function]]
| Parses a string containing a date, and returns the number of milliseconds between that date and midnight, January 1, 1970.
|-
| [[javascript/Date/UTC|Date.UTC Function]]
| Returns the number of milliseconds between midnight, January 1, 1970 Universal Coordinated Time (UTC) (or GMT) and the supplied date.
|}
==Methods==
The following table lists methods of the '''Date Object'''.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Date/getDate|getDate Method]]
| Returns the day-of-the-month value using local time.
|-
| [[javascript/Date/getDay|getDay Method]]
| Returns the day-of-the-week value using local time.
|-
| [[javascript/Date/getFullYear|getFullYear Method]]
| Returns the year value using local time.
|-
| [[javascript/Date/getHours|getHours Method]]
| Returns the hours value using local time.
|-
| [[javascript/Date/getMilliseconds|getMilliseconds Method]]
| Returns the milliseconds value using local time.
|-
| [[javascript/Date/getMinutes|getMinutes Method]]
| Returns the minutes value using local time.
|-
| [[javascript/Date/getMonth|getMonth Method]]
| Returns the month value using local time.
|-
| [[javascript/Date/getSeconds|getSeconds Method]]
| Returns seconds value using local time.
|-
| [[javascript/Date/getTime|getTime Method]]
| Returns the time value in a Date Object as the number of milliseconds since midnight January 1, 1970.
|-
| [[javascript/Date/getTimezoneOffset|getTimezoneOffset Method]]
| Returns the difference in minutes between the time on the host computer and Universal Coordinated Time (UTC).
|-
| [[javascript/Date/getUTCDate|getUTCDate Method]]
| Returns the day-of-the-month value using UTC.
|-
| [[javascript/Date/getUTCDay|getUTCDay Method]]
| Returns the day-of-the-week value using UTC.
|-
| [[javascript/Date/getUTCFullYear|getUTCFullYear Method]]
| Returns the year value using UTC.
|-
| [[javascript/Date/getUTCHours|getUTCHours Method]]
| Returns the hours value using UTC.
|-
| [[javascript/Date/getUTCMilliseconds|getUTCMilliseconds Method]]
| Returns the milliseconds value using UTC.
|-
| [[javascript/Date/getUTCMinutes|getUTCMinutes Method]]
| Returns the minutes value using UTC.
|-
| [[javascript/Date/getUTCMonth|getUTCMonth Method]]
| Returns the month value using UTC.
|-
| [[javascript/Date/getUTCSeconds|getUTCSeconds Method]]
| Returns the seconds value using UTC.
|-
| [[javascript/Date/getYear|getYear Method]]
| Returns the year value .
|-
| [[javascript/Object/hasOwnProperty|hasOwnProperty Method]]
| Returns a Boolean value that indicates whether an object has a property with the specified name.
|-
| [[javascript/Object/isPrototypeOf|isPrototypeOf Method]]
| Returns a Boolean value that indicates whether an object exists in another object's prototype chain.
|-
| [[javascript/Object/propertyIsEnumerable|propertyIsEnumerable Method]]
| Returns a Boolean value that indicates whether a specified property is part of an object and whether it is enumerable.
|-
| [[javascript/Date/setDate|setDate Method]]
| Sets the numeric day of the month using local time.
|-
| [[javascript/Date/setFullYear|setFullYear Method]]
| Sets the year value using local time.
|-
| [[javascript/Date/setHours|setHours Method]]
| Sets the hours value using local time.
|-
| [[javascript/Date/setMilliseconds|setMilliseconds Method]]
| Sets the milliseconds value using local time.
|-
| [[javascript/Date/setMinutes|setMinutes Method]]
| Sets the minutes value using local time.
|-
| [[javascript/Date/setMonth|setMonth Method]]
| Sets the month value using local time.
|-
| [[javascript/Date/setSeconds|setSeconds Method]]
| Sets the seconds value using local time.
|-
| [[javascript/Date/setTime|setTime Method]]
| Sets the date and time value in the Date object.
|-
| [[javascript/Date/setUTCDate|setUTCDate Method]]
| Sets the numeric day of the month using UTC.
|-
| [[javascript/Date/setUTCFullYear|setUTCFullYear Method]]
| Sets the year value using UTC.
|-
| [[javascript/Date/setUTCHours|setUTCHours Method]]
| Sets the hours value using UTC.
|-
| [[javascript/Date/setUTCMilliseconds|setUTCMilliseconds Method]]
| Sets the milliseconds value using UTC.
|-
| [[javascript/Date/setUTCMinutes|setUTCMinutes Method]]
| Sets the minutes value using UTC.
|-
| [[javascript/Date/setUTCMonth|setUTCMonth Method]]
| Sets the month value using UTC.
|-
| [[javascript/Date/setUTCSeconds|setUTCSeconds Method]]
| Sets the seconds value using UTC.
|-
| [[javascript/Date/setYear|setYear Method]]
| Sets the year value using local time.
|-
| [[javascript/Date/toDateString|toDateString Method]]
| Returns a date as a string value.
|-
| [[javascript/Date/toGMTString|toGMTString Method]]
| Returns a date converted to a string using Greenwich Mean Time (GMT).
|-
| [[javascript/Date/toISOString|toISOString Method]]
| Returns a date as a string value in ISO format.
|-
| [[javascript/Date/toJSON|toJSON Method]]
| Used to transform data of an object type before the JSON serialization.
|-
| [[javascript/Date/toLocaleDateString|toLocaleDateString Method]]
| Returns a date as a string value appropriate to the host environment's current locale.
|-
| [[javascript/Object/toLocaleString|toLocaleString Method]]
| Returns an object converted to a string using the current locale.
|-
| [[javascript/Date/toLocaleTimeString|toLocaleTimeString Method]]
| Returns a time as a string value appropriate to the host environment's current locale.
|-
| [[javascript/Date/toString|toString Method]]
| Returns a string representation of an object.
|-
| [[javascript/Date/toTimeString|toTimeString Method]]
| Returns a time as a string value.
|-
| [[javascript/Date/toUTCString|toUTCString Method]]
| Returns a date converted to a string using UTC.
|-
| [[javascript/Date/valueOf|valueOf Method]]
| Returns the primitive value of the specified object.
|}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/cd9w2te4(v=vs.94).aspx
|HTML5Rocks_link=
}}