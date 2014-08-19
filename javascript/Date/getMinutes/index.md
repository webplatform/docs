{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the minutes of a Date object, using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getMinutes()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an integer between 0 and 59. Zero is returned the time is less than one minute after the hour. If a '''Date''' object was created without specifying the time, by default the minute value is 0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to the '''getMinutes''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date.getMinutes());
 document.write("&lt;br/&gt;");
 
 date.setMinutes(5);
 document.write(date.getMinutes());
 
 // Output:
 // 0
 // 5
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the minutes value using Universal Coordinated Time (UTC), use the '''getUTCMinutes''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCMinutes{{!}}getUTCMinutes Method (Date)]]
* [[javascript/Date/setMinutes{{!}}setMinutes Method (Date)]]
* [[javascript/Date/setUTCMinutes{{!}}setUTCMinutes Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/t919zcb7(v=vs.94).aspx
|HTML5Rocks_link=
}}