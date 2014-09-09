{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns the stored time value in milliseconds since midnight, January 1, 1970 UTC.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=date.valueOf()
}}
|Values=
}}
{{JS_Return_Value
|Description=The stored time value in milliseconds since midnight, January 1, 1970 UTC. This is the same value as '''getTime'''. The date object is any instance of a Date.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''valueOf''' method with a date.
|Code=var myDate = new Date();
 myDate.setFullYear(2100, 5, 5);
 if (myDate.getTime() == myDate.valueOf())
     document.write("values are the same");
 else
     document.write("values are different");
 
 // Output: values are the same
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155184(v=vs.94).aspx
|HTML5Rocks_link=
}}