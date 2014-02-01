{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the stored time value in milliseconds since midnight, January 1, 1970 UTC.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= date.valueOf()}}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The date object is any instance of a Date.}}
}}
{{JS_Return_Value
|Description=The stored time value in milliseconds since midnight, January 1, 1970 UTC. This is the same value as '''getTime'''.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''valueOf''' method with a date.

|Code= var myDate = new Date();
 myDate.setFullYear(2100, 5, 5);
 if (myDate.getTime() == myDate.valueOf())
     document.write("values are the same");
 else
     document.write("values are different");
 
 // Output: values are the same
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155184(v=vs.94).aspx
|HTML5Rocks_link=
}}