{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the month of a Date object using Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getUTCMonth() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=Returns an integer between 0 (January) and 11 (December).}}
{{Remarks_Section
|Remarks=To get the month in local time, use the '''getMonth''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''getUTCMonth''' method.

|Code= var date = new Date("2/2/2002");
 document.write(date.getUTCMonth());
 
 // Output: 1
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMonth{{!}}getMonth Method (Date)]]
* [[javascript/Date/setMonth{{!}}setMonth Method (Date)]]
* [[javascript/Date/setUTCMonth{{!}}setUTCMonth Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hkd7k0a3(v=vs.94).aspx
|HTML5Rocks_link=
}}