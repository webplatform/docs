{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the month of a Date object using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getUTCMonth()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns an integer between 0 (January) and 11 (December).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''getUTCMonth''' method.
|Code=var date = new Date("2/2/2002");
 document.write(date.getUTCMonth());
 
 // Output: 1
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the month in local time, use the '''getMonth''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMonth{{!}}getMonth Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hkd7k0a3(v=vs.94).aspx
|HTML5Rocks_link=
}}