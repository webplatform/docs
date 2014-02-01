{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the day of the week, using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj. getDay() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a '''Date''' object.}}
}}
{{JS_Return_Value
|Description=An integer between 0 and 6 representing the day of the week (Sunday is 0, Saturday is 6).}}
{{Remarks_Section
|Remarks=To get the day using Universal Coordinated Time (UTC), use the '''getUTCDay''' method.

The following example shows how to use the '''getDay''' method.

 var date = new Date("Saturday, February 9, 2008");
 day = date.getDay();
 document.write(day);
 
 // Output: 6
}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCDay{{!}}getUTCDay Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/5wtd2bt8(v=vs.94).aspx
|HTML5Rocks_link=
}}