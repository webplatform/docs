{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Rename the page to 'comment' instead of 'Comment'
|Checked_Out=No
}}
{{Summary_Section|Causes comments to be ignored by the JavaScript parser.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Single-line Comment:
// comment
}}{{JS Syntax Format
|Format=Multiline Comment:
/*
comment
*/
}}{{JS Syntax Format
|Format=Comments with conditional compilation:
//@CondStatement
/*@
condStatement
@*/
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the most common uses of comments.
|Code=/* This is a multiline comment that
     can span as many lines as necessary.  */
 function myfunction(arg1, arg2){
     var r;
     // This is a single line comment.
     r = arg1 + arg2
     return(r);
 }
}}{{Single Example
|Language=JavaScript
|Description=The following example shows how to use conditional compilation. This example uses special comment delimiters that are used only if conditional compilation is activated by the @cc_on statement. Scripting engines that do not support conditional compilation see only the message that says conditional compilation is not supported.
|Code=/*@cc_on @*/
 /*@if (@_jscript_version &gt;= 4)
     alert("JavaScript version 4 or better");
     @else @*/
     alert("Conditional compilation not supported by this scripting engine.");
 /*@end @*/
}}
}}
{{Remarks_Section
|Remarks=The comment argument is the text of any comment you want to include in your script. The condStatement argument is to be used if conditional compilation is activated. If single-line comments are used, there can be no space between the "//" and "@" characters.

Use comments to keep parts of a script from being read by the JavaScript parser. You can use comments to include explanatory remarks in a program.

If single-line comments are used, the parser ignores any text between the comment marker and the end of the line. If multi-line comments are used, the parser ignores any text between the beginning and end markers.

Comments are used to support conditional compilation while retaining compatibility with browsers that do not support that feature. These browsers treat those forms of comments as single-line or multi-line comments respectively.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}