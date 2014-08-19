{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the month, using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getMonth()
}}
|Values=
}}
{{JS_Return_Value
|Description=The '''getMonth''' method returns an integer between 0 (January) and 11 (December). For a '''Date''' constructed with "Jan 5, 1996", '''getMonth''' returns 0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getMonth''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date.getMonth());
 
 // Output: 0
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the month value using Universal Coordinated Time (UTC), use the '''getUTCMonth''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCMonth{{!}}getUTCMonth Method (Date)]]
* [[javascript/Date/setMonth{{!}}setMonth Method (Date)]]
* [[javascript/Date/setUTCMonth{{!}}setUTCMonth Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/z284z68x(v=vs.94).aspx
|HTML5Rocks_link=
}}