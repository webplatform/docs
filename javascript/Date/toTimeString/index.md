{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a time as a string value.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= objDate. toTimeString( )}}
}}
{{Remarks_Section
|Remarks=The required objDate reference is a Date object.

The '''toTimeString''' method returns a string value containing the time in the current time zone.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=In the following example, the time is set to 2000 milliseconds after midnight January 1, 1970 UTC, and then it is written out.

|Code= var aDate = new Date();
      aDate.setTime(2000);
      document.write(aDate.toTimeString());
 
 // Output depends on the time in the current time zone.
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toDateString{{!}}toDateString Method (Date)]]
* [[javascript/Date/toLocaleTimeString{{!}}toLocaleTimeString Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/y3xxxf8e(v=vs.94).aspx
|HTML5Rocks_link=
}}