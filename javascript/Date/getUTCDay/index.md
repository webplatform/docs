{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the day of the week using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getUTCDay()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an integer between 0 (Sunday) and 6 (Saturday) that represents the day of the week.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getUTCDay''' method.
|Code=var date = new Date("2/6/2001");
 var day = date.getUTCDay();
 document.write(day);
 
 // Output: 2
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the day of the week using local time, use the '''getDate''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getDay{{!}}getDay Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/aexkzf1c(v=vs.94).aspx
|HTML5Rocks_link=
}}