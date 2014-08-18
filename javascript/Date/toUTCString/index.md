{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a date converted to a string using Universal Coordinated Time (UTC).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''toUTCString()'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toUTCString''' method.
|Code=function toUTCStrDemo(){
    var d, s;                   //Declare variables.
    d = new Date();             //Create Date object.
    s = "Current setting is ";
    s += d.toUTCString() ;       //Convert to UTC string.
    return(s);                  //Return UTC string.
 }
}}
}}
{{Remarks_Section
|Remarks=The required dateObj reference is any Date object.

The '''toUTCString''' method returns a String object that contains the date formatted using UTC convention in a convenient, easily read form.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toGMTString{{!}}toGMTString Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7ew14035(v=vs.94).aspx
|HTML5Rocks_link=
}}