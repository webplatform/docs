{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Establishes the default object for a statement. Disallowed in [[javascript/directives/use_strict|strict mode]].}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=with ( object ) {
     statements
}
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=
|Description=The new default object.
}}{{JS Syntax Parameter
|Name=statements
|Required=
|Description=One or more statements for which object is the default object.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The with statement is commonly used to shorten the amount of code that you have to write in certain situations. In this example, notice the repeated use of Math.

When you use the '''with''' statement, your code may become shorter and easier to read (yet with uncommon semantics).
|Code=// Not using 'with'.
var x = Math.cos(3 * Math.PI) + Math.sin(Math.LN10);
var y = Math.tan(14 * Math.E);

// Using 'with'.
var x, y;
with (Math) {
    x = cos(3 * PI) + sin (LN10);
    y = tan(14 * E);
}
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=The following strict mode code will cause a syntax error to be thrown, because '''with''' statements are disallowed in strict mode.
|Code="use strict";
with (Math) {
    console.log(cos(3));
}
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
This statement changes the default context from a global or a function scope, to one of a given context.
Every variable declared within the body of this statement (within the curly brackets) is defined on the given context instead of on the function or global scope.


This statement is disallowed in [[javascript/directives/use_strict|strict mode]] and so will generate a syntax error before even running the script.
{{See_Also_Section
|Manual_links=* [[javascript/statements/this{{!}}this Statement]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/b294afx9(v=vs.94).aspx
|HTML5Rocks_link=
}}