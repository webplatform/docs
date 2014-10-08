{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns a date converted to a string formatted according to UTC conventions.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toUTCString()
}}
|Values=
}}
{{JS_Return_Value
|Description=String that contains the date formatted using UTC conventions: <code>Fri, 09 May 2014 00:00:00 GMT</code>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var date = new Date("2014-05-09");
console.log(date.toUTCString()); // "Fri, 09 May 2014 00:00:00 GMT"
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks='''UTC''' is the acronym of Universal Coordinated Time.

The Format returned by this ''toGMTString'' was defined by [http://tools.ietf.org/html/rfc822#section-5] and was refined by  [http://tools.ietf.org/html/rfc1123#section-5.2.14 RFC-1123]
}}
{{Notes_Section
|Usage=
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
* [[javascript/Date/toLocaleDateString{{!}}toLocaleDateString Method (Date)]]
* [[javascript/Date/toTimeString{{!}}toTimeString Method (Date)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toUTCString toUTCString(), by Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/7ew14035%28v=vs.94%29.aspx toUTCString(), by Microsoft Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.42 Date.prototype.toUTCString( )]

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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7ew14035(v=vs.94).aspx
|HTML5Rocks_link=
}}