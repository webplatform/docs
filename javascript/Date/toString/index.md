{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a string representation of a date. The format of the string depends on the locale. For U.S. English (en-us), it is as follows:

day of the week month day hour : minute : second time zone year

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= date.toString()}}
|Values={{JS_Syntax_Parameter
|Name=date
|Required=Required
|Description=The date to represent as a string.}}
}}
{{JS_Return_Value
|Description=Returns the string representation of the date.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toString''' method with a date.

|Code= var myDate = new Date();
 myDate.setFullYear(2100, 5, 5);
 var dateString = myDate.toString();
 document.write(dateString);
 
 // Output: &lt;date&gt;
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155294(v=vs.94).aspx
|HTML5Rocks_link=
}}