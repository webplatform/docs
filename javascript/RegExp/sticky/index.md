{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs to be moved under javascript/RegExp
|Checked_Out=No
}}
{{Summary_Section|Returns a Boolean value indicating the state of the sticky flag ( '''y''' ) used with a regular expression. Default is <code>false</code>. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=rgExp.'''sticky'''
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
|Code=var stickyglobal = /foo.bar/gy;

stickyglobal.test('foo*bar');
// → true
stickyglobal.lastIndex;
// → 7
stickyglobal.test('..foo*bar');
// → false

stickyglobal.lastIndex = 0;
stickyglobal.test("..foo*bar");
// → false

stickyglobal.lastIndex = 2;
stickyglobal.test("..foo*bar");
// → true
stickyglobal.lastIndex;
// → 9
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The <code>sticky</code> property returns <code>true</code> if the sticky flag is set for a regular expression, and returns <code>false</code> if it is not.

The <code>sticky</code> flag, when used, indicates …
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