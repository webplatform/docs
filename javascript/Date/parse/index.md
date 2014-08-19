{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Parses a string containing a date, and returns the number of milliseconds between that date and midnight, January 1, 1970.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Date.parse( dateVal )
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Date.parse''' function.
|Code=var dateString = "November 1, 1997 10:15 AM";
 var mSec = Date.parse(dateString);
 document.write(mSec);
 // Output: 878404500000
}}{{Single Example
|Language=JavaScript
|Description=The following example returns the difference between the date provided and 1/1/1970.
|Code=var minMilli = 1000 * 60;    
 var hrMilli = minMilli * 60;
 var dyMilli = hrMilli * 24;
 
 var ms = Date.parse(new Date("June 1, 1990"));
 var days = Math.round(ms / dyMilli);
 
 var dateStr = "";
 dateStr += "There are " + days + " days ";
 dateStr += "between 01/01/1970 and " + testDate;
 document.write(dateStr);
 
 // Output: There are 7456 days between 01/01/1970 and Fri Jun 1 00:00:00 PDT 1990
}}
}}
{{Remarks_Section
|Remarks=The required dateVal argument is either a string containing a date or a VT_DATE value retrieved from an ActiveX object or other object. For information about date strings that the '''Date.parse''' function can parse. see Formatting Date and Time Strings (Windows Scripting - JScript).

The '''Date.parse''' function returns an integer value representing the number of milliseconds between midnight, January 1, 1970 and the date supplied in dateVal.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getDate{{!}}getDate Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/k4w173wk(v=vs.94).aspx
|HTML5Rocks_link=
}}