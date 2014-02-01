{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the day-of-the-month, using Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getUTCDate() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=Returns an integer between 1 and 31 that represents the day-of-the-month.}}
{{Remarks_Section
|Remarks=To get the day of the month using local time, use the '''getDate''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''getUTCDate''' method.

|Code= var date = new Date("1/23/2001");
 document.write(date.getUTCDate());
 
 // Output: 23
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getDate{{!}}getDate Method (Date)]]
* [[javascript/Date/setDate{{!}}setDate Method (Date)]]
* [[javascript/Date/setUTCDate{{!}}setUTCDate Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/z8d0k600(v=vs.94).aspx
|HTML5Rocks_link=
}}