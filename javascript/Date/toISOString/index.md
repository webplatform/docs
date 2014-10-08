{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns a date as a string value in simplified ISO 8601 Extended format.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toISOString()
}}
|Values=
}}
{{JS_Return_Value
|Description=String in simplified [http://en.wikipedia.org/wiki/ISO_8601 ISO 8601 Extended] format: <code>YYYY-MM-DDTHH:mm:ss.sssZ</code>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var now = new Date();
console.log(date.toISOString());
// ouputs: "2014-10-08T12:54:27.487Z"
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=Manually assembling the ISO 8601 format (polyfill)
|Code=// if the environment does not support toISOString() yet
// add it to the Date prototype
if (!Date.prototype.toISOString) {
  Date.prototype.toISOString = (function() {
    function twoDigits(value) {
      return (value < 10 ? '0' : ') + value;
    }

    return function toISOString() {
      return this.getUTCFullYear()
        + '-' + twoDigits(this.getUTCMonth() + 1)
        + '-' + twoDigits(this.getUTCDate())
        + 'T' + twoDigits(this.getUTCHours())
        + ':' + twoDigits(this.getUTCMinutes())
        + ':' + twoDigits(this.getUTCSeconds())
        + '.' + (this.getUTCMilliseconds() / 1000).toFixed(3).slice(2, 5)
        + 'Z';
    };
  })();
}
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks====Throws===

[[javascript/Error|<code>RangeError</code>]] when called on a date object with an ''invalid date'' (e.g. <code>new Date("I am not a date");</code> - see [http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.1.1 Time Values And Time Range])
}}
{{Notes_Section
|Usage=The ISO 8601 Extended format is supported by [[javascript/Date/parse|Date.parse()]], it is therefore a good choice when dates need to be exchanged between APIs.
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/toString{{!}}toString Method (Date)]]
* [[javascript/Date/toDateString{{!}}toDateString Method (Date)]]
* [[javascript/Date/toGMTString{{!}}toGMTString Method (Date)]]
* [[javascript/Date/toLocaleString{{!}}toLocaleString Method (Date)]]
* [[javascript/Date/toLocaleDateString{{!}}toLocaleDateString Method (Date)]]
* [[javascript/Date/toLocaleTimeString{{!}}toLocaleTimeString Method (Date)]]
* [[javascript/Date/toTimeString{{!}}toTimeString Method (Date)]]
* [[javascript/Date/toUTCString{{!}}toUTCString Method (Date)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toISOString toISOString(), by Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ff925953%28v=vs.94%29.aspx toISOString(), by Microsoft Developer Network]
* [http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.1.15 Date Time String Format, ECMAScript 5.1]
* [http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.1.1 Time Values and Time Range, ECMAScript 5.1]
* [http://en.wikipedia.org/wiki/ISO_8601 ISO 8601, Wikipedia]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.43 Date.prototype.toISOString()]

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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff925953(v=vs.94).aspx
|HTML5Rocks_link=
}}