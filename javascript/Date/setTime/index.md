{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the date and time value in the Date object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.'''setTime(''' milliseconds ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.}}{{JS_Syntax_Parameter
|Name=milliseconds
|Required=Required
|Description=A numeric value representing the number of elapsed milliseconds since midnight, January 1, 1970 GMT.}}
}}
{{Remarks_Section
|Remarks=If milliseconds is negative, it indicates a date before 1970. The range of available dates is approximately 285,616 years from either side of 1970.

Setting the date and time with the '''setTime''' method is independent of the time zone.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''setTime''' method.

|Code= function SetTimeTest(newtime){
    var d, s;                  //Declare variables.
    d = new Date();            //Create Date object.d.setTime( newtime ) ;        //Set time.
    s = "Current setting is ";
    s += d.toUTCString();
    return(s);                 //Return new setting.
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getTime{{!}}getTime Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/767045xx(v=vs.94).aspx
|HTML5Rocks_link=
}}