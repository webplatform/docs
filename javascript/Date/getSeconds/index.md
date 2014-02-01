{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the seconds of a '''Date''' object, using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getSeconds() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=Returns an integer between 0 and 59. Zero is returned when the time is less than one second into the current minute. If a '''Date''' object was created without specifying the time, by default the seconds value is 0.}}
{{Remarks_Section
|Remarks=To get the seconds value using Universal Coordinated Time (UTC), use the '''getUTCSeconds''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''getSeconds''' method.

|Code= var date = new Date("1/1/2001");
 document.write(date.getSeconds());
 document.write("&lt;br/&gt;");
 
 date.setSeconds(5);
 document.write(date.getSeconds());
 
 // Output:
 // 0
 // 5
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCSeconds{{!}}getUTCSeconds Method (Date)]]
* [[javascript/Date/setSeconds{{!}}setSeconds Method (Date)]]
* [[javascript/Date/setUTCSeconds{{!}}setUTCSeconds Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ct79zx09(v=vs.94).aspx
|HTML5Rocks_link=
}}