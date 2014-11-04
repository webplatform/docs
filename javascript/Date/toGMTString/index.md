{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns a date converted to a string formatted according to GMT conventions.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toGMTString()
}}
|Values=
}}
{{JS_Return_Value
|Description=String that contains the date formatted using GMT conventions: <code>Fri, 09 May 2014 00:00:00 GMT</code>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var date = new Date("2014-05-09");
console.log(date.toGMTString()); // "Fri, 09 May 2014 00:00:00 GMT"
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks='''GMT''' is the acronym of Greenwich Mean Time.

The Format returned by this ''toGMTString'' was defined by [http://tools.ietf.org/html/rfc822#section-5] and was refined by  [http://tools.ietf.org/html/rfc1123#section-5.2.14 RFC-1123]
}}
{{Notes_Section
|Usage=
|Notes=The '''toGMTString''' method is obsolete, and is provided for backwards compatibility only. It is recommended that you use the [[javascript/Date/toUTCString{{!}}toUTCString]] method instead.

According to the specification, ''toGMTString'' and ''toUTCString'' should be the same function. This is not true in Google Chrome and Internet Explorer, yet both functions return the same result.
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toString{{!}}toString Method (Date)]]
* [[javascript/Date/toDateString{{!}}toDateString Method (Date)]]
* [[javascript/Date/toISOString{{!}}toISOString Method (Date)]]
* [[javascript/Date/toLocaleString{{!}}toLocaleString Method (Date)]]
* [[javascript/Date/toLocaleDateString{{!}}toLocaleDateString Method (Date)]]
* [[javascript/Date/toLocaleTimeString{{!}}toLocaleTimeString Method (Date)]]
* [[javascript/Date/toTimeString{{!}}toTimeString Method (Date)]]
* [[javascript/Date/toUTCString{{!}}toUTCString Method (Date)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toGMTString toGMTString(), by Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/a34ehb82%28v=vs.94%29.aspx toGMTString(), by Microsoft Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-B.2.6 Date.prototype.toGMTString( )]

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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/a34ehb82(v=vs.94).aspx
|HTML5Rocks_link=
}}