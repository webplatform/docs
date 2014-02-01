{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the year, using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getFullYear() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=The year as a four-digit number. For example, the year 1976 is returned as 1976. Years specified as two digits in the '''Date''' constructor or in '''setFullYear''' are assumed to be in the twentieth century, so given "5/14/12", '''getFullYear''' returns "1912".}}
{{Remarks_Section
|Remarks=To get the year using Universal Coordinated Time (UTC), use the '''getUTCFullYear''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''getFullYear''' method.

|Code= var date = new Date("1/1/01");
 document.write(date.getFullYear());
 
 // Output: 1901
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getUTCFullYear{{!}}getUTCFullYear Method (Date)]]
* [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]]
* [[javascript/Date/setUTCFullYear{{!}}setUTCFullYear Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/29y2w2x3(v=vs.94).aspx
|HTML5Rocks_link=
}}