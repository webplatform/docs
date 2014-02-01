{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the month, using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getMonth() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=The '''getMonth''' method returns an integer between 0 (January) and 11 (December). For a '''Date''' constructed with "Jan 5, 1996", '''getMonth''' returns 0.}}
{{Remarks_Section
|Remarks=To get the month value using Universal Coordinated Time (UTC), use the '''getUTCMonth''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''getMonth''' method.

|Code= var date = new Date("1/1/2001");
 document.write(date.getMonth());
 
 // Output: 0
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCMonth{{!}}getUTCMonth Method (Date)]]
* [[javascript/Date/setMonth{{!}}setMonth Method (Date)]]
* [[javascript/Date/setUTCMonth{{!}}setUTCMonth Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/z284z68x(v=vs.94).aspx
|HTML5Rocks_link=
}}