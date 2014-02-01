{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the year of the '''Date''' object using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.setFullYear( numYear [, numMonth [, numDate ]]) }}
|Values={{JS_Syntax_Parameter
|Name=dateObj
|Required=Required
|Description=Any '''Date''' object.}}{{JS_Syntax_Parameter
|Name=numYear
|Required=Required
|Description=A numeric value for the year.}}{{JS_Syntax_Parameter
|Name=numMonth
|Required=Optional
|Description=A zero-based numeric value for the month (0 for January, 11 for December). Must be specified if numDate is specified.}}{{JS_Syntax_Parameter
|Name=numDate
|Required=Optional
|Description=A numeric value equal for the day of the month.}}
}}
{{Remarks_Section
|Remarks=All '''set''' methods taking optional arguments use the value returned from corresponding '''get''' methods, if you do not specify the optional argument. For example, if the numMonth argument is optional, but not specified, JavaScript uses the value returned from the '''getMonth''' method.

In addition, if the value of an argument is greater than its calendar range or is negative, the date rolls forward or backward as appropriate.

To set the year using Universal Coordinated Time (UTC), use the '''setUTCFullYear''' method.

The range of years supported in the date object is approximately 285,616 years before and after 1970.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setFullYear''' method:

|Code= var date1 = new Date("1/1/2001");
 date1.setFullYear(2007);
 
 var date2 = new Date("1/1/2001");
 date2.setFullYear(2008, 10, 3); 
 
 document.write (date1.toLocaleString());
 document.write ("&lt;br /&gt;");
 document.write (date2.toLocaleString());
 
 // Output:
 // Monday, January 01, 2007 12:00:00 AM
 // Monday, November 03, 2008 12:00:00 AM
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getFullYear{{!}}getFullYear Method (Date)]]
* [[javascript/Date/getUTCFullYear{{!}}getUTCFullYear Method (Date)]]
* [[javascript/Date/setUTCFullYear{{!}}setUTCFullYear Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/y367b7x8(v=vs.94).aspx
|HTML5Rocks_link=
}}