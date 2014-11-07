{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Declares a variable.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=var variable = value;
}}
|Values={{JS Syntax Parameter
|Name=variable
|Required=
|Description=The name of the variable being declared.
}}{{JS Syntax Parameter
|Name=value
|Required=
|Description=The initial value assigned to the variable.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following examples illustrate the use of the var statement.
|Code=var index;
var name = 'Thomas Jefferson';
var answer = 42,
    counter,
    numpages = 10;
var array = [];
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=Use the <code>var</code> statement to declare variables. You can assign values to the variables when you declare them or later in your script.

A variable is declared the first time it appears in your script.

You can declare a variable without using the <code>var</code> keyword and assign a value to it. This is known as an implicit declaration, and it is not recommended. An implicit declaration gives the variable global scope. When you declare a variable at the procedure level, though, you typically do not want it to have global scope, because that means other scripts could overwrite it causing your script to break.. To avoid giving the variable global scope, you must use the <code>var</code> keyword in your variable declaration.

If you do not initialize your variable in the <code>var</code> statement, it is automatically assigned [[javascript/undefined{{!}}the JavaScript value <code>undefined</code>]].
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
* [[javascript/operators/new{{!}}new Operator]]
* [[javascript/Array{{!}}Array Object]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/z16cackw(v=vs.94).aspx
|HTML5Rocks_link=
}}