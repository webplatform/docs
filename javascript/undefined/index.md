{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed import
|Checked_Out=No
}}
{{Summary_Section|A value that has never been defined, such as a variable that has not been initialized.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=undefined
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Usage of '''undefined''' with strict equality.
|Code=var foo;

if (foo === undefined) {
    // executes
} else {
   // won't execute
}
}}{{Single Example
|Language=JavaScript
|Description=Usage of '''undefined''' with the [[javascript/operators/typeof{{!}}typeof Operator]].
|Code=var foo;

if (typeof foo === "undefined") {
    // executes
} else {
   // won't execute
}
}}{{Single Example
|Language=JavaScript
|Description=Comparison of strict equality and the [[javascript/operators/typeof{{!}}typeof Operator]]. Typeof doesn't throw an error if the variable hasn't been defined.
|Code=// foo variable is not defined
if (typeof foo === "undefined") {
    // executes
}

if (foo === undefined) {
    // throws ReferenceError
}
}}
}}
{{Remarks_Section
|Remarks=The '''undefined''' constant is a member of the '''Global''' object, and becomes available when the scripting engine is initialized. When a variable has been declared but not initialized, its value is '''undefined'''.

If a variable has not been declared, you cannot compare it to '''undefined''' , but you can compare the type of the variable to the string "undefined". (see second example)

The '''undefined''' constant is useful when explicitly testing or setting a variable to undefined.
}}
{{Notes_Section
|Usage='''undefined''' is not a reserved word, thus can be used as a variable in any scope except for the global scope.
|Notes==='''undefined''' vs. '''null'''==
'''undefined''' means a value is declared but not initialized, it doesn't have a value assigned to it.

[[javascript/null{{!}}null]] can be assigned to a variable to represent no value.

Other than that, '''undefined''' is a type, while '''null''' is an object
}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/operators/typeof{{!}}typeof Operator]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dae3sbk5(v=vs.94).aspx
|HTML5Rocks_link=
}}