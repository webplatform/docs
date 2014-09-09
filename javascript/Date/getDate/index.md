{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Gets the day-of-the-month, using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getDate()
}}
|Values=
}}
{{JS_Return_Value
|Description=An integer between 1 and 31 that represents the day-of-the-month.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getDate''' method.
|Code=var date = new Date("Jan 01, 2001");
 var str = "Today's date is: ";
    str += (date.getMonth() + 1) + "/";
    str += date.getDate() + "/";
    str += date.getFullYear();
 document.write(str);
 
 // Output: Today's date is: 1/1/2001
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the day-of-the-month using Universal Coordinated Time (UTC), use the '''getUTCDate''' method.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCDate{{!}}getUTCDate Method (Date)]]
* [[javascript/Date/setDate{{!}}setDate Method (Date)]]
* [[javascript/Date/setUTCDate{{!}}setUTCDate Method (Date)]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Date
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/217fw5tk(v=vs.94).aspx
|HTML5Rocks_link=
}}