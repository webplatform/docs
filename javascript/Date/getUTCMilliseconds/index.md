{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the milliseconds of a Date object using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getUTCMilliseconds()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns a millisecond value that can range from 0-999.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getUTCMilliseconds''' method.
|Code=var date = new Date("1/1/2001");
 document.write(date.getUTCMilliseconds());
 document.write("&lt;br/&gt;");
 
 date.setMilliseconds(34);
 document.writedate.getUTCMilliseconds());
 
 // Output:
 // 0 
 // 34
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is a '''Date''' object. To get the number of milliseconds in local time, use the '''getMilliseconds''' method.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMilliseconds{{!}}getMilliseconds Method (Date)]]
* [[javascript/Date/setMilliseconds{{!}}setMilliseconds Method (Date)]]
* [[javascript/Date/setUTCMilliseconds{{!}}setUTCMilliseconds Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/tkx22wzs(v=vs.94).aspx
|HTML5Rocks_link=
}}