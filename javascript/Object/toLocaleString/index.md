{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns a date converted to a string using the current locale.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''toLocaleString()'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toLocaleString''' method.
|Code=function toLocaleStrDemo(){   
    var d, s;                      //Declare variables.
    d = new Date();                //Create Date object.
    s = "Current setting is ";
    s += d.toLocaleString() ;       //Convert to current locale.
    return(s);                     //Return converted date
 }
}}
}}
{{Remarks_Section
|Remarks=The required dateObj is any Date object.

The '''toLocaleString''' method returns a String object that contains the date written in the current locale's long default format.

* For dates between 1601 and 1999 A.D., the date is formatted according to the user's Control Panel Regional Settings.
* For dates outside this range, the default format of the '''toString''' method is used.
For example, in the United States, '''toLocaleString''' returns "01/05/96 00:00:00" for January 5. In Europe, it returns "05/01/96 00:00:00" for the same date, as European convention puts the day before the month.

'''Note''' -- '''toLocaleString''' should only be used to display results to a user; it should never be used as the basis for computation within a script as the returned result is machine-specific.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.3 15.4.4.3 Array.prototype.toLocaleString ( )]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Array
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/wb66sb9s(v=vs.94).aspx
|HTML5Rocks_link=
}}