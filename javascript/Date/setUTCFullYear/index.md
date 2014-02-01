{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the year value in the Date object using Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.'''setUTCFullYear(''' numYear [ ''', ''' numMonth [ ''',''' numDate ]] ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.}}{{JS_Syntax_Parameter
|Name=numYear
|Required=Required
|Description=A numeric value equal to the year.}}{{JS_Syntax_Parameter
|Name=numMonth
|Required=Optional
|Description=A numeric value equal to the month. The value for January is 0, and other month values follow consecutively. Must be supplied if numDate is supplied.}}{{JS_Syntax_Parameter
|Name=numDate
|Required=Optional
|Description=A numeric value equal to the day of the month.}}
}}
{{Remarks_Section
|Remarks=All '''set''' methods taking optional arguments use the value returned from corresponding '''get''' methods, if you do not specify an optional argument. For example, if the numMonth argument is not specified, JavaScript uses the value returned from the '''getUTCMonth''' method.

In addition, if the value of an argument is greater that its range or is a negative number, other stored values are modified accordingly.

To set the year using local time, use the '''setFullYear''' method.

The range of years supported in the Date object is approximately 285,616 years from either side of 1970.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setUTCFullYear''' method.

|Code= var dtFirst = new Date();
 dtFirst.setUTCFullYear(2007);
 
 var dtSecond = new Date();
 // 10 is the value for November. 
 dtSecond.setUTCFullYear(2008, 10, 3); 
 
 document.write (dtFirst.toUTCString());
 document.write ("&lt;br /&gt;");
 document.write (dtSecond.toUTCString());
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getFullYear{{!}}getFullYear Method (Date)]]
* [[javascript/Date/getUTCFullYear{{!}}getUTCFullYear Method (Date)]]
* [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/c9sd3ksb(v=vs.94).aspx
|HTML5Rocks_link=
}}