{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the day-of-the-month, using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getDate() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=An integer between 1 and 31 that represents the day-of-the-month.}}
{{Remarks_Section
|Remarks=To get the day-of-the-month using Universal Coordinated Time (UTC), use the '''getUTCDate''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getDate''' method.

|Code= var date = new Date("Jan 01, 2001");
 var str = "Today's date is: ";
    str += (date.getMonth() + 1) + "/";
    str += date.getDate() + "/";
    str += date.getFullYear();
 document.write(str);
 
 // Output: Today's date is: 1/1/2001
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCDate{{!}}getUTCDate Method (Date)]]
* [[javascript/Date/setDate{{!}}setDate Method (Date)]]
* [[javascript/Date/setUTCDate{{!}}setUTCDate Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/217fw5tk(v=vs.94).aspx
|HTML5Rocks_link=
}}