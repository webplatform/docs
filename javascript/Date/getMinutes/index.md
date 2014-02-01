{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the minutes of a Date object, using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getMinutes() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=Returns an integer between 0 and 59. Zero is returned the time is less than one minute after the hour. If a '''Date''' object was created without specifying the time, by default the minute value is 0.}}
{{Remarks_Section
|Remarks=To get the minutes value using Universal Coordinated Time (UTC), use the '''getUTCMinutes''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to the '''getMinutes''' method.

|Code= var date = new Date("1/1/2001");
 document.write(date.getMinutes());
 document.write("&lt;br/&gt;");
 
 date.setMinutes(5);
 document.write(date.getMinutes());
 
 // Output:
 // 0
 // 5
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCMinutes{{!}}getUTCMinutes Method (Date)]]
* [[javascript/Date/setMinutes{{!}}setMinutes Method (Date)]]
* [[javascript/Date/setUTCMinutes{{!}}setUTCMinutes Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/t919zcb7(v=vs.94).aspx
|HTML5Rocks_link=
}}