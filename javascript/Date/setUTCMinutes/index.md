{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Sets the minutes value in the Date object using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''setUTCMinutes(''' numMinutes [ ''',''' numSeconds [ ''',''' numMilli ]] ''')'''
}}
|Values={{JS Syntax Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.
}}{{JS Syntax Parameter
|Name=numMinutes
|Required=Required
|Description=A numeric value equal to the minutes value. Must be supplied if either of the following arguments is used.
}}{{JS Syntax Parameter
|Name=numSeconds
|Required=Optional
|Description=A numeric value equal to the seconds value. Must be supplied if numMilli is used.
}}{{JS Syntax Parameter
|Name=numMilli
|Required=Optional
|Description=A numeric value equal to the milliseconds value.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setUTCMinutes''' method:
|Code=function SetUTCMinutesDemo(nmin, nsec){
    var d, s;                    // Declare variables.
    d = new Date();              // Create Date object.d.setUTCMinutes( nmin,nsec ) ;  // Set UTC minutes.
    s = "Current setting is " + d.toUTCString() 
    return(s);                   // Return new setting.
 }
}}
}}
{{Remarks_Section
|Remarks=All '''set''' methods taking optional arguments use the value returned from corresponding '''get''' methods, if you do not specify an optional argument. For example, if the numSeconds argument is not specified, JavaScript uses the value returned from the '''getUTCSeconds''' method.

To modify the minutes value using local time, use the '''setMinutes''' method.

If the value of an argument is greater than its range, or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00.00", and '''setUTCMinutes(70)''' is called, the date is changed to "Jan 5, 1996 01:10:00.00."

The '''setUTCHours''' method can be used to set the hours, minutes, seconds, and milliseconds.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMinutes{{!}}getMinutes Method (Date)]]
* [[javascript/Date/getUTCMinutes{{!}}getUTCMinutes Method (Date)]]
* [[javascript/Date/setMinutes{{!}}setMinutes Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/esssx44h(v=vs.94).aspx
|HTML5Rocks_link=
}}