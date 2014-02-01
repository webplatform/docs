{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a date as a string value appropriate to the host environment's current locale.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= objDate.'''toLocaleDateString( )'''}}
}}
{{Remarks_Section
|Remarks=The required objDate reference is a Date object.

The '''toLocaleDateString''' method returns a string value that contains a date, in the current time zone, in an easily read format. The date is in the default format of the host environment's current locale. The return value of this method cannot be relied upon in scripting, as it will vary from computer to computer. The '''toLocaleDateString''' method should only be used to format display - never as part of a computation.
}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toDateString{{!}}toDateString Method (Date)]]
* [[javascript/Date/toLocaleTimeString{{!}}toLocaleTimeString Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/kecw102f(v=vs.94).aspx
|HTML5Rocks_link=
}}