{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs to be moved under javascript/RegExp
|Checked_Out=No
}}
{{Summary_Section|Returns a Boolean value indicating the state of the Unicode flag (<code>u</code>) used with a regular expression. Default is <code>false</code>. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=regex.'''unicode'''
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the Unicode property.
|Code=// https://mathiasbynens.be/notes/es6-unicode-regex#impact-dot
// Note: `𝌆` is U+1D306 TETRAGRAM FOR CENTRE, a supplementary Unicode symbol.
var string = 'a𝌆b';

console.log(/a.b/.unicode);
// → false

console.log(/a.b/.test(string));
// → false

console.log(/a.b/u.unicode);
// → true

console.log(/a.b/u.test(string));
// → true

var match = string.match(/a(.)b/u);
console.log(match[1]);
// → '𝌆'
|LiveURL=https://mathiasbynens.be/notes/es6-unicode-regex#impact-dot
}}
}}
{{Remarks_Section
|Remarks=The <code>unicode</code> property returns <code>true</code> if the Unicode flag is set for a regular expression, and returns <code>false</code> if it is not.

The Unicode flag, when used, enables [https://mathiasbynens.be/notes/es6-unicode-regex various Unicode-related features for regular expressions], such as the use of ES6 Unicode code point escapes (e.g. <code>/\u{1D306}/u</code>).
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Topic_clusters=Javascript
|Manual_links=* [[javascript/regular expression/global{{!}}global Property (Regular Expression)]]
* [[javascript/regular expression/ignoreCase{{!}}ignoreCase Property (Regular Expression)]]
* [[javascript/regular expression/multiline{{!}}multiline Property (Regular Expression)]]
* [[javascript/regular expression/sticky{{!}}sticky Property (Regular Expression)]]
|External_links=* [https://mathiasbynens.be/notes/es6-unicode-regex Unicode-aware regular expressions in ECMAScript 6]
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Property
|Applies to=RegExp
}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}