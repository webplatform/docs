{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the seconds of a '''Date''' object using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getUTCSeconds()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an integer between 0 and 59. Zero is returned when the time is less than one second into the current minute. If a '''Date''' object was created without specifying the time, by default the UTC seconds value is 0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getUTCSeconds''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date. getUTCSeconds());
 
 // Output: 0
}}
}}
{{Remarks_Section
|Remarks=To get the number of seconds in local time, use the '''getSeconds''' method. The required dateObj reference is a '''Date''' object.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getSeconds{{!}}getSeconds Method (Date)]]
* [[javascript/Date/setSeconds{{!}}setSeconds Method (Date)]]
* [[javascript/Date/setUTCSeconds{{!}}setUTCSeconds Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/4y0y6x01(v=vs.94).aspx
|HTML5Rocks_link=
}}