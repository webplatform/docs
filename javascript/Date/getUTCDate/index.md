{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the day-of-the-month, using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getUTCDate()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an integer between 1 and 31 that represents the day-of-the-month.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getUTCDate''' method.
|Code=var date = new Date("1/23/2001");
 document.write(date.getUTCDate());
 
 // Output: 23
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the day of the month using local time, use the '''getDate''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getDate{{!}}getDate Method (Date)]]
* [[javascript/Date/setDate{{!}}setDate Method (Date)]]
* [[javascript/Date/setUTCDate{{!}}setUTCDate Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/z8d0k600(v=vs.94).aspx
|HTML5Rocks_link=
}}