{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=An Internationalization/Localization center should be build to cover the basic concepts (like locale) so this stuff doesn't have to be repeated over and over
|Checked_Out=No
}}
{{Summary_Section|Returns a date as a string value appropriate to the host environment's current locale.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toLocaleDateString()
}}
|Values=
}}
{{JS_Return_Value
|Description=String that contains a date, in the current time zone, in a human readable format. The date is in the default format of the host environment's current locale.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var nowdate = new Date();
alert(nowdate.toLocaleDateString());
// output: "Tuesday, November 04, 2014"

|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=The return value of '''toLocaleDateString''' cannot be relied upon in scripting, as it will vary from computer to computer. The '''toLocaleDateString''' method should only be used to format display - never as part of a computation.
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toString{{!}}toString Method (Date)]]
* [[javascript/Date/toDateString{{!}}toDateString Method (Date)]]
* [[javascript/Date/toGMTString{{!}}toGMTString Method (Date)]]
* [[javascript/Date/toISOString{{!}}toISOString Method (Date)]]
* [[javascript/Date/toLocaleString{{!}}toLocaleString Method (Date)]]
* [[javascript/Date/toLocaleTimeString{{!}}toLocaleTimeString Method (Date)]]
* [[javascript/Date/toTimeString{{!}}toTimeString Method (Date)]]
* [[javascript/Date/toUTCString{{!}}toUTCString Method (Date)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString toDateTimeString(), by Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/kecw102f(v=vs.94).aspx toDateTimeString(), by Microsoft Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.6 Date.prototype.toLocaleDateString()]

ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Date
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/kecw102f(v=vs.94).aspx
|HTML5Rocks_link=
}}