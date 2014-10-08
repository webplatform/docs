{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns a human readbale string representation of a date.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toString()
}}
|Values=
}}
{{JS_Return_Value
|Description=String that contains the date, time and timezone in a human readable format.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var now = new Date();
console.log(now.toString()); 
// outputs: "Wed Oct 08 2014 13:46:37 GMT+0200 (CEST)"
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=
|Notes=According to the specification the contents of the String are implementation-dependent. That means that you cannot rely on the returned format being consistent across browsers. That said, all major browsers seem to agree on the format <code>Wed Oct 08 2014 13:46:37 GMT+0200 (CEST)</code>.

''toString()'' adds the code of the current timezone to the output. Because the output format is not specified, some browsers might replace <code>(CEST)</code> (Central European Summer Time) with a fully localized text, e.g. the German <code>(Mitteleuropäische Sommerzeit)</code>.
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toDateString{{!}}toDateString Method (Date)]]
* [[javascript/Date/toGMTString{{!}}toGMTString Method (Date)]]
* [[javascript/Date/toISOString{{!}}toISOString Method (Date)]]
* [[javascript/Date/toLocaleDateString{{!}}toLocaleDateString Method (Date)]]
* [[javascript/Date/toTimeString{{!}}toTimeString Method (Date)]]
* [[javascript/Date/toUTCString{{!}}toUTCString Method (Date)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toString toString(), by Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/jj155294%28v=vs.94%29.aspx toUTCString(), by Microsoft Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.2 Date.prototype.toString()]

ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155294(v=vs.94).aspx
|HTML5Rocks_link=
}}