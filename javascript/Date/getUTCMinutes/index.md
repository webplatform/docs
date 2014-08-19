{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the minutes of a Date object using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getUTCMinutes()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an integer between 0 and 59. Zero is returned the time is less than one minute after the hour. If a '''Date''' object was created without specifying the time, by default the UTC minute value is 0. However, in other time zones it may be different.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getUTCMinutes''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date.getUTCMinutes());
 document.write("&lt;br/&gt;");
 
 date.setMinutes(5);
 document.write(date.getUTCMinutes());
 
 // Output: 
 // 0
 // 5
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the number of minutes stored using local time, use the '''getMinutes''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMinutes{{!}}getMinutes Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7xt0y1cc(v=vs.94).aspx
|HTML5Rocks_link=
}}