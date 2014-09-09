{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Gets the year, using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getFullYear()
}}
|Values=
}}
{{JS_Return_Value
|Description=The year as a four-digit number. For example, the year 1976 is returned as 1976. Years specified as two digits in the '''Date''' constructor or in '''setFullYear''' are assumed to be in the twentieth century, so given "5/14/12", '''getFullYear''' returns "1912".
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getFullYear''' method.
|Code=var date = new Date("1/1/01");
 document.write(date.getFullYear());
 
 // Output: 1901
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the year using Universal Coordinated Time (UTC), use the '''getUTCFullYear''' method.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCFullYear{{!}}getUTCFullYear Method (Date)]]
* [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]]
* [[javascript/Date/setUTCFullYear{{!}}setUTCFullYear Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/29y2w2x3(v=vs.94).aspx
|HTML5Rocks_link=
}}