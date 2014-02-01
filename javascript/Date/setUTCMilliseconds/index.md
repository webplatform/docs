{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the milliseconds value in the Date object using Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.'''setUTCMilliseconds(''' numMilli ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.}}{{JS_Syntax_Parameter
|Name=numMilli
|Required=Required
|Description=A numeric value equal to the millisecond value.}}
}}
{{Remarks_Section
|Remarks=To set the milliseconds using local time, use the '''setMilliseconds''' method.

If the value of numMilli is greater than 999, or is a negative number, the stored number of seconds (and minutes, hours, and so forth, if necessary) is incremented an appropriate amount.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setUTCMilliseconds''' method.

|Code= function SetUTCMSecDemo(nmsec){   
 // Create Date object.
    var d = new Date();           
 // Set UTC milliseconds.
    d.setUTCMilliseconds(nmsec);  
 
    var s = "Current setting is ";
    s += d.toUTCString();
    s += " and " + d.getUTCMilliseconds();
    s += " milliseconds"
    return(s);
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getMilliseconds{{!}}getMilliseconds Method (Date)]]
* [[javascript/Date/getUTCMilliseconds{{!}}getUTCMilliseconds Method (Date)]]
* [[javascript/Date/setMilliseconds{{!}}setMilliseconds Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ytffzy7a(v=vs.94).aspx
|HTML5Rocks_link=
}}