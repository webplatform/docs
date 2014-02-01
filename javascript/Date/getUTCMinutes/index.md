{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the minutes of a Date object using Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getUTCMinutes() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=Returns an integer between 0 and 59. Zero is returned the time is less than one minute after the hour. If a '''Date''' object was created without specifying the time, by default the UTC minute value is 0. However, in other time zones it may be different.}}
{{Remarks_Section
|Remarks=To get the number of minutes stored using local time, use the '''getMinutes''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getUTCMinutes''' method.

|Code= var date = new Date("1/1/2001");
 document.write(date.getUTCMinutes());
 document.write("&lt;br/&gt;");
 
 date.setMinutes(5);
 document.write(date.getUTCMinutes());
 
 // Output: 
 // 0
 // 5
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMinutes{{!}}getMinutes Method (Date)]]
* [[javascript/Date/setMinutes{{!}}setMinutes Method (Date)]]
* [[javascript/Date/setUTCMinutes{{!}}setUTCMinutes Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7xt0y1cc(v=vs.94).aspx
|HTML5Rocks_link=
}}