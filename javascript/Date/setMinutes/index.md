{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the minutes value in the '''Date''' object using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.'''setMinutes(''' numMinutes [ ''', ''' numSeconds [ ''', ''' numMilli ]] ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.}}{{JS_Syntax_Parameter
|Name=numMinutes
|Required=Required
|Description=A numeric value equal to the minutes value. Must be supplied if either of the following arguments is used.}}{{JS_Syntax_Parameter
|Name=numSeconds
|Required=Optional
|Description=A numeric value equal to the seconds value. Must be supplied if the numMilli argument is used.}}{{JS_Syntax_Parameter
|Name=numMilli
|Required=Optional
|Description=A numeric value equal to the milliseconds value.}}
}}
{{Remarks_Section
|Remarks=All '''set''' methods taking optional arguments use the value returned from corresponding '''get''' methods, if you do not specify an optional argument. For example, if the numSeconds argument not specified, JavaScript uses the value returned from the '''getSeconds''' method.

To set the minutes value using Universal Coordinated Time (UTC), use the '''setUTCMinutes''' method.

If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00" and '''setMinutes(90)''' is called, the date is changed to "Jan 5, 1996 01:30:00." Negative numbers have a similar behavior.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setMinutes''' method.

|Code= function SetMinutesDemo(nmin, nsec){
    var d, s;                     // Declare variables.
    d = new Date();               // Create Date object.d.setMinutes( nmin , nsec ) ;     // Set minutes.
    s = "Current setting is " + d.toLocaleString() 
    return(s);                    // Return new setting.
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMinutes{{!}}getMinutes Method (Date)]]
* [[javascript/Date/getUTCMinutes{{!}}getUTCMinutes Method (Date)]]
* [[javascript/Date/setUTCMinutes{{!}}setUTCMinutes Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/3sbd2ey3(v=vs.94).aspx
|HTML5Rocks_link=
}}