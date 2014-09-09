{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Sets the numeric day-of-the-month value of the '''Date''' object using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.setDate( numDate ''')'''
}}
|Values={{JS Syntax Parameter
|Name=dateObj
|Required=Required
|Description=Any '''Date''' object.
}}{{JS Syntax Parameter
|Name=numDate
|Required=Required
|Description=A numeric value equal to the day of the month.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''setDate''' method.
|Code=var date = new Date("12/15/1990");
 date.setDate(30);
 document.write(date);
 
 // Output (for the PST time zone): Sun Dec 30 00:00:00 PST 1990
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=To set the day-of-the-month value using Universal Coordinated Time (UTC), use the '''setUTCDate''' method.

If the value of numDate is greater than the number of days in the month, the date rolls over to a later month and/or year. For example, if the stored date is January 5, 1996 and '''setDate(32)''' is called, the date changes to February 1, 1996. If numDate is a negative number, the date rolls back to an earlier month and/or year. For example, if the stored date is January 5, 1996 and '''setDate(-32)''' is called, the date changes to November 29, 1995.

The [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]] can be used to set the year, month, and day of the month.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getDate{{!}}getDate Method (Date)]]
* [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]]
* [[javascript/Date/setMonth{{!}}setMonth Method (Date)]]
* [[javascript/Date/setUTCDate{{!}}setUTCDate Method (Date)]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Date
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/txfkf2t2(v=vs.94).aspx
|HTML5Rocks_link=
}}