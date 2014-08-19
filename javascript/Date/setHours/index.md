{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Sets the hour value in the Date object using local time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''setHours(''' numHours [ ''',''' numMin [ ''',''' numSec [ ''',''' numMilli ]]] ''')'''
}}
|Values={{JS Syntax Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.
}}{{JS Syntax Parameter
|Name=numHours
|Required=Required
|Description=A numeric value equal to the hours value.
}}{{JS Syntax Parameter
|Name=numMin
|Required=Optional
|Description=A numeric value equal to the minutes value. Must be supplied if either of the following arguments is used.
}}{{JS Syntax Parameter
|Name=numSec
|Required=Optional
|Description=A numeric value equal to the seconds value. Must be supplied if the following argument is used.
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
|Description=The following example illustrates the use of the '''setHours''' method.
|Code=function SetHoursDemo(nhr, nmin, nsec){
    var d, s;                     //Declare variables.
    d = new Date();               //Create Date object.d.setHours( nhr , nmin , nsec ) ;  //Set hours, minutes, &amp; seconds.
    s = "Current setting is " + d.toLocaleString() 
    return(s);                    //Return new date setting.
 }
}}
}}
{{Remarks_Section
|Remarks=All '''set''' methods taking optional arguments use the value returned from corresponding '''get''' methods, if you do not specify an optional argument. For example, if the numMinutes argument is not specified, JavaScript uses the value returned from the '''getMinutes''' method.

To set the hours value using Universal Coordinated Time (UTC), use the '''setUTCHours''' method.

If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00", and '''setHours(30)''' is called, the date is changed to "Jan 6, 1996 06:00:00." Negative numbers have a similar behavior.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getHours{{!}}getHours Method (Date)]]
* [[javascript/Date/getUTCHours{{!}}getUTCHours Method (Date)]]
* [[javascript/Date/setUTCHours{{!}}setUTCHours Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/f4a5xhxy(v=vs.94).aspx
|HTML5Rocks_link=
}}