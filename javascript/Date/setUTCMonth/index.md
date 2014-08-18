{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Sets the month value in the Date object using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''setUTCMonth(''' numMonth [ ''',''' dateVal ] ''')'''
}}
|Values={{JS Syntax Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.
}}{{JS Syntax Parameter
|Name=numMonth
|Required=Required
|Description=A numeric value equal to the month. The value for January is 0, and other month values follow consecutively.
}}{{JS Syntax Parameter
|Name=dateVal
|Required=Optional
|Description=A numeric value representing the day of the month. If it is not supplied, the value from a call to the '''getUTCDate''' method is used.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setUTCMonth''' method.
|Code=function SetUTCMonthDemo(newmonth){
    var d, s;                       // Declare variables.
    d = new Date();                 // Create Date object.d.setUTCMonth( newmonth ) ;        // Set UTC month.
    s = "Current setting is ";
    s += d.toUTCString(); 
    return(s);                      // Return new setting.
 }
}}
}}
{{Remarks_Section
|Remarks=To set the month value using local time, use the '''setMonth''' method.

If the value of numMonth is greater than 11 (January is month 0), or is a negative number, the stored year is incremented or decremented appropriately. For example, if the stored date is "Jan 5, 1996 00:00:00.00", and '''setUTCMonth(14)''' is called, the date is changed to "Mar 5, 1997 00:00:00.00."

The '''setUTCFullYear''' method can be used to set the year, month, and day of the month.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMonth{{!}}getMonth Method (Date)]]
* [[javascript/Date/getUTCMonth{{!}}getUTCMonth Method (Date)]]
* [[javascript/Date/setMonth{{!}}setMonth Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/d82ks7xe(v=vs.94).aspx
|HTML5Rocks_link=
}}