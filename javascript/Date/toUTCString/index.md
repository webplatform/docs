{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a date converted to a string using Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.'''toUTCString()''' }}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is any Date object.

The '''toUTCString''' method returns a String object that contains the date formatted using UTC convention in a convenient, easily read form.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toUTCString''' method.

|Code= function toUTCStrDemo(){
    var d, s;                   //Declare variables.
    d = new Date();             //Create Date object.
    s = "Current setting is ";
    s += d.toUTCString() ;       //Convert to UTC string.
    return(s);                  //Return UTC string.
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toGMTString{{!}}toGMTString Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7ew14035(v=vs.94).aspx
|HTML5Rocks_link=
}}