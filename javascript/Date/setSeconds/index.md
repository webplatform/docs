{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the seconds value in the Date object using local time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj '''.setSeconds(''' numSeconds [ ''',''' numMilli ] ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.}}{{JS_Syntax_Parameter
|Name=numSeconds
|Required=Required
|Description=A numeric value equal to the seconds value.}}{{JS_Syntax_Parameter
|Name=numMilli
|Required=Optional
|Description=A numeric value equal to the milliseconds value.}}
}}
{{Remarks_Section
|Remarks=All '''set''' methods taking optional arguments use the value returned from corresponding '''get''' methods, if you do not specify an optional argument. For example, if the numMilli argument is not specified, JavaScript uses the value returned from the '''getMilliseconds''' method.

To set the seconds value using Universal Coordinated Time (UTC), use the '''setUTCSeconds''' method.

If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00" and '''setSeconds(150)''' is called, the date is changed to "Jan 5, 1996 00:02:30."

The setHours method can be used to set the hours, minutes, seconds, and milliseconds.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setSeconds''' method.

|Code= function SetSecondsDemo(nsec){
    var d = new Date();         //Create Date object.d.setSeconds( nsec ) ;         //Set seconds.
    var s = "Current setting is ";
    s += d.toLocaleString();
    return(s);                  //Return new setting.
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getSeconds{{!}}getSeconds Method (Date)]]
* [[javascript/Date/getUTCSeconds{{!}}getUTCSeconds Method (Date)]]
* [[javascript/Date/setUTCSeconds{{!}}setUTCSeconds Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/df6eb6zf(v=vs.94).aspx
|HTML5Rocks_link=
}}