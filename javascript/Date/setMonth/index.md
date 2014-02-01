{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the month value in the '''Date''' object using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj. setMonth( numMonth [ ''',''' dateVal ]) }}
|Values={{JS_Syntax_Parameter
|Name=dateObj
|Required=Required
|Description=Any '''Date''' object.}}{{JS_Syntax_Parameter
|Name=numMonth
|Required=Required
|Description=A numeric value equal to the month. The value for January is 0, and other month values follow consecutively.}}{{JS_Syntax_Parameter
|Name=dateVal
|Required=Optional
|Description=A numeric value representing the day of the month. If this value is not supplied, the value from a call to the '''getDate''' method is used.}}
}}
{{Remarks_Section
|Remarks=To set the month value using Universal Coordinated Time (UTC), use the '''setUTCMonth''' method.

If the value of numMonth is greater than 11 (January is month 0) or is a negative number, the stored year is modified accordingly. For example, if the stored date is "Jan 5, 1996" and '''setMonth(14)''' is called, the date is changed to "Mar 5, 1997."

The '''setFullYear''' method can be used to set the year, month, and day of the month.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setMonth''' method.

|Code= date = new Date('1/1/1990');
 date.setMonth(14);
 document.write(date);
 
 // Output: Fri Mar 1 00:00:00 PST 1991
 // Note that the time zone corresponds to the time zone on the local computer.
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMonth{{!}}getMonth Method (Date)]]
* [[javascript/Date/getUTCMonth{{!}}getUTCMonth Method (Date)]]
* [[javascript/Date/setUTCMonth{{!}}setUTCMonth Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/tst8h9zw(v=vs.94).aspx
|HTML5Rocks_link=
}}