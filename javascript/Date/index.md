---
title: Date
tags:
  0: JS
  1: Basic
  3: Object
readiness: 'Ready to Use'
summary: 'Enables basic storage and retrieval of dates and times.'
uri: javascript/Date

---
# Date

## Summary

Enables basic storage and retrieval of dates and times.

## Syntax

    dateObj = new Date()

    dateObj = new Date( dateVal )

    dateObj = new Date( year , month , date [, hours [, minutes [, seconds [, ms ]]]])

**dateObj**
:   Required. The variable name to which the Date object is assigned.

**dateVal**
:   Required. If a numeric value, dateVal represents the number of milliseconds in Universal Coordinated Time between the specified date and midnight January 1, 1970. If a string, dateVal is parsed according to the rules in Formatting Date and Time Strings (Windows Scripting - JScript). The dateVal argument can also be a VT\_DATE value as returned from some ActiveX objects.

**year**
:   Required. The full year, for example, 1976 (and not 76).

**month**
:   Required. The month as an integer between 0 and 11 (January to December).

**date**
:   Required. The date as an integer between 1 and 31.

**hours**
:   Optional. Must be supplied if minutes is supplied. An integer from 0 to 23 (midnight to 11pm) that specifies the hour.

**minutes**
:   Optional. Must be supplied if seconds is supplied. An integer from 0 to 59 that specifies the minutes.

**seconds**
:   Optional. Must be supplied if milliseconds is supplied. An integer from 0 to 59 that specifies the seconds.

**ms**
:   Optional. An integer from 0 to 999 that specifies the milliseconds.

## Examples

The following example illustrates the use of the Date object.

``` {.js}
var dateString = "Today's date is: ";

 var newDate = new Date();

 // Get the month, day, and year.
 dateString += (newDate.getMonth() + 1) + "/";
 dateString += newDate.getDate() + "/";
 dateString += newDate.getFullYear();

 document.write(dateString);

 // Output: Today's date is: <date>
```

## Remarks

A Date object contains a number representing a particular instant in time to within a millisecond. If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if you specify 150 seconds, JavaScript redefines that number as two minutes and 30 seconds.

If the number is **NaN** , the object does not represent a specific instant of time. If you pass no parameters to the Date object, it is initialized to the current time (UTC). A value must be given to the object before you can use it.

The range of dates that can be represented in a Date object is approximately 285,616 years on either side of January 1, 1970.

See Date and Time Calculations (Windows Scripting - JScript) for more information about how to use the Date object and related methods.

## Properties

The following table lists the properties of the **Date** object.

## Functions

The following table lists the functions of the **Date** object.

## Methods

The following table lists the methods of the **Date** object.

Method
:   Summary
[getDate](/javascript/Date/getDate)
:   Gets the day-of-the-month, using local time.
[getDay](/javascript/Date/getDay)
:   Gets the day of the week, using local time.
[getFullYear](/javascript/Date/getFullYear)
:   Gets the year, using local time.
[getHours](/javascript/Date/getHours)
:   Gets the hours in a date, using local time.
[getMilliseconds](/javascript/Date/getMilliseconds)
:   Gets the milliseconds of a Date, using local time.
[getMinutes](/javascript/Date/getMinutes)
:   Gets the minutes of a Date object, using local time.
[getMonth](/javascript/Date/getMonth)
:   Gets the month, using local time.
[getSeconds](/javascript/Date/getSeconds)
:   Gets the seconds of a **Date** object, using local time.
[getTime](/javascript/Date/getTime)
:   Gets the time value in milliseconds.
[getTimezoneOffset](/javascript/Date/getTimezoneOffset)
:   Gets the difference in minutes between the time on the local computer and Universal Coordinated Time (UTC).
[getUTCDate](/javascript/Date/getUTCDate)
:   Gets the day-of-the-month, using Universal Coordinated Time (UTC).
[getUTCDay](/javascript/Date/getUTCDay)
:   Gets the day of the week using Universal Coordinated Time (UTC).
[getUTCFullYear](/javascript/Date/getUTCFullYear)
:   Gets the year using Universal Coordinated Time (UTC).
[getUTCHours](/javascript/Date/getUTCHours)
:   Gets the hours value in a **Date** object using Universal Coordinated Time (UTC).
[getUTCMilliseconds](/javascript/Date/getUTCMilliseconds)
:   Gets the milliseconds of a Date object using Universal Coordinated Time (UTC).
[getUTCMinutes](/javascript/Date/getUTCMinutes)
:   Gets the minutes of a Date object using Universal Coordinated Time (UTC).
[getUTCMonth](/javascript/Date/getUTCMonth)
:   Gets the month of a Date object using Universal Coordinated Time (UTC).
[getUTCSeconds](/javascript/Date/getUTCSeconds)
:   Gets the seconds of a **Date** object using Universal Coordinated Time (UTC).
[getYear](/javascript/Date/getYear)
:   Gets the year of a **Date** object. Deprecated in favor of **getFullYear** method.
[setDate](/javascript/Date/setDate)
:   Sets the numeric day-of-the-month value of the **Date** object using local time.
[setFullYear](/javascript/Date/setFullYear)
:   Sets the year of the **Date** object using local time.
[setHours](/javascript/Date/setHours)
:   Sets the hour value in the Date object using local time.
[setMilliseconds](/javascript/Date/setMilliseconds)
:   Sets the milliseconds value in the Date object using local time.
[setMinutes](/javascript/Date/setMinutes)
:   Sets the minutes value in the **Date** object using local time.
[setMonth](/javascript/Date/setMonth)
:   Sets the month value in the **Date** object using local time.
[setSeconds](/javascript/Date/setSeconds)
:   Sets the seconds value in the Date object using local time.
[setTime](/javascript/Date/setTime)
:   Sets the date and time value in the Date object.
[setUTCDate](/javascript/Date/setUTCDate)
:   Sets the numeric day of the month in the Date object using Universal Coordinated Time (UTC).
[setUTCFullYear](/javascript/Date/setUTCFullYear)
:   Sets the year value in the Date object using Universal Coordinated Time (UTC).
[setUTCHours](/javascript/Date/setUTCHours)
:   Sets the hours value in the Date object using Universal Coordinated Time (UTC).
[setUTCMilliseconds](/javascript/Date/setUTCMilliseconds)
:   Sets the milliseconds value in the Date object using Universal Coordinated Time (UTC).
[setUTCMinutes](/javascript/Date/setUTCMinutes)
:   Sets the minutes value in the Date object using Universal Coordinated Time (UTC).
[setUTCMonth](/javascript/Date/setUTCMonth)
:   Sets the month value in the Date object using Universal Coordinated Time (UTC).
[setUTCSeconds](/javascript/Date/setUTCSeconds)
:   Sets the seconds value in the Date object using Universal Coordinated Time (UTC).
[setYear](/javascript/Date/setYear)
:   Sets the year value in the **Date** object. Deprecated in favor of the **setFullYear** method.
[toDateString](/javascript/Date/toDateString)
:   Returns the date component of a date as a human readable string.
[toGMTString](/javascript/Date/toGMTString)
:   Returns a date converted to a string formatted according to GMT conventions.
[toISOString](/javascript/Date/toISOString)
:   Returns a date as a string value in simplified ISO 8601 Extended format.
[toLocaleDateString](/javascript/Date/toLocaleDateString)
:   Returns a date as a string value appropriate to the host environment's current locale.
[toTimeString](/javascript/Date/toTimeString)
:   Returns the time component of a date as a human readable string.
[toUTCString](/javascript/Date/toUTCString)
:   Returns a date converted to a string formatted according to UTC conventions.
[valueOf](/javascript/Date/valueOf)
:   Returns the stored time value in milliseconds since midnight, January 1, 1970 UTC.
[hasOwnProperty](/javascript/Object/hasOwnProperty)
:   Determines whether an object has a property with the specified name.
[isPrototypeOf](/javascript/Object/isPrototypeOf)
:   Determines whether an object exists in another object's prototype chain.

## Properties

The following table lists properties of the **Date Object**.

Property
:   Description
[constructor](/javascript/Date/constructor)
:   Specifies the function that creates an object.
[prototype](/javascript/Date/prototype)
:   Returns a reference to the prototype for a class of objects.

## Functions

The following table lists functions of the **Date Object**.

Functions
:   Description
[Date.now](/javascript/Date/now)
:   Returns the number of milliseconds between January 1, 1970, and the current date and time.
[Date.parse](/javascript/Date/parse)
:   Parses a string containing a date, and returns the number of milliseconds between that date and midnight, January 1, 1970.
[Date.UTC](/javascript/Date/UTC)
:   Returns the number of milliseconds between midnight, January 1, 1970 Universal Coordinated Time (UTC) (or GMT) and the supplied date.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/cd9w2te4(v=vs.94).aspx)

