{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Sets the milliseconds value in the Date object using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''setMilliseconds(''' numMilli ''')'''
}}
|Values={{JS Syntax Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.
}}{{JS Syntax Parameter
|Name=numMilli
|Required=Required
|Description=A numeric value equal to the millisecond value.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setMilliseconds''' method.
|Code=function SetMSecDemo(nmsec){
    var d, s;                    // Declare variables.
    d = new Date();              // Create Date object.d.setMilliseconds( nmsec ) ;    // Set milliseconds.
    s = "Current setting is ";
    s += d.toLocaleString();
    s += " and " + d.getMilliseconds();
    s += " milliseconds";
    return(s);                   // Return new date setting.
 }
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=To set the milliseconds value using Universal Coordinated Time (UTC), use the '''setUTCMilliseconds''' method.

If the value of numMilli is greater than 999 or is a negative number, the stored number of seconds (and minutes, hours, and so forth if necessary) is incremented an appropriate amount.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMilliseconds{{!}}getMilliseconds Method (Date)]]
* [[javascript/Date/getUTCMilliseconds{{!}}getUTCMilliseconds Method (Date)]]
* [[javascript/Date/setUTCMilliseconds{{!}}setUTCMilliseconds Method (Date)]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/a92fx7ha(v=vs.94).aspx
|HTML5Rocks_link=
}}