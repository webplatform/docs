{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Moved under javascript/RegExp
|Checked_Out=No
}}
{{Summary_Section|Returns a Boolean value indicating the state of the sticky flag ( '''y''' ) used with a regular expression. Default is <code>false</code>. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=regex.'''sticky'''
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
|Description=The following example illustrates the use of the <code>sticky</code> property.
|Code=var regex = /foo.bar/gy;
regex.sticky;
// → true
regex.lastIndex;
// → 0

regex.test('foo*bar');
// → true
regex.lastIndex;
// → 7
regex.test('..foo*bar');
// → false

regex.lastIndex = 0;
regex.test('..foo*bar');
// → false

regex.lastIndex = 2;
regex.test('..foo*bar');
// → true
regex.lastIndex;
// → 9
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The <code>sticky</code> property returns <code>true</code> if the sticky flag is set for a regular expression, and returns <code>false</code> if it is not.

The <code>sticky</code> flag, when used, indicates that the regular expression performs sticky matching in the target string by attempting to match starting at <code>lastIndex</code>. If matching at that location fails, then <code>null</code> is returned, i.e., no forward “anchoring” search is performed. If matching succeeds, then the regular expression’s <code>lastIndex</code> property is updated as for the flag <code>g</code>.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/global{{!}}global Property (Regular Expression)]]
* [[javascript/regular expression/ignoreCase{{!}}ignoreCase Property (Regular Expression)]]
* [[javascript/regular expression/multiline{{!}}multiline Property (Regular Expression)]]
* [[javascript/regular expression/unicode{{!}}unicode Property (Regular Expression)]]
|External_links=
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