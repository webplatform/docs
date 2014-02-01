{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the year using Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getUTCFullYear() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=Returns the year as a four-digit number. Years specified as two digits in the '''Date''' constructor or in '''setFullYear''' are assumed to be in the twentieth century, so given "5/14/12", '''getUTCFullYear''' returns "1912".}}
{{Remarks_Section
|Remarks=To get the year using local time, use the '''getFullYear''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''getUTCFullYear''' method.

|Code= var date = new Date("1/9/36");
 document.write(date.getUTCFullYear());
 
 // Output: 1936
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getFullYear{{!}}getFullYear Method (Date)]]
* [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]]
* [[javascript/Date/setUTCFullYear{{!}}setUTCFullYear Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/47f8w843(v=vs.94).aspx
|HTML5Rocks_link=
}}