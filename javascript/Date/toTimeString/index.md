{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns the time component of a date as a human readable string.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toTimeString()
}}
|Values=
}}
{{JS_Return_Value
|Description=String value containing the time, in the current time zone, in a convenient, human readable format, e.g. <code>15:20:46 GMT+0200 (CEST)</code>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var date = new Date();
console.log(date.toTimeString());
// outputs: "15:20:46 GMT+0200 (CEST)"
console.log(now.toString()); 
// outputs: "Wed Oct 08 2014 15:20:46 GMT+0200 (CEST)"
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=
|Notes=According to the specification the contents of the String are implementation-dependent. That means that you cannot rely on the returned format being consistent across browsers. That said, all major browsers seem to agree on the format <code>15:20:46 GMT+0200 (CEST)</code>

''toTimeString()'' adds the code of the current timezone to the output. Because the output format is not specified, some browsers might replace <code>(CEST)</code> (Central European Summer Time) with a fully localized text, e.g. the German <code>(Mitteleuropäische Sommerzeit)</code>.
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
* [[javascript/Date/toLocaleDateString{{!}}toLocaleDateString Method (Date)]]
* [[javascript/Date/toLocaleTimeString{{!}}toLocaleTimeString Method (Date)]]
* [[javascript/Date/toUTCString{{!}}toUTCString Method (Date)]]

|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toTimeString toTimeString(), by Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/y3xxxf8e%28v=vs.94%29.aspx toTimeString(), by Microsoft Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.4 Date.prototype.toTimeString()]

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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/y3xxxf8e(v=vs.94).aspx
|HTML5Rocks_link=
}}