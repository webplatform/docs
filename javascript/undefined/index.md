{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|A value that has never been defined, such as a variable that has not been initialized.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=undefined
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
|Description=Usage of '''undefined''' with strict equality.
|Code=var foo;

if (foo === undefined) {
    // executes
} else {
   // won't execute
}
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=Usage of <code>undefined</code> with the [[javascript/operators/typeof{{!}}typeof operator]].
|Code=var foo;

if (typeof foo === 'undefined') {
    // executes
} else {
   // won't execute
}
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=Comparison of strict equality and the [[javascript/operators/typeof{{!}}typeof operator]]. <code>typeof</code> doesn’t throw an error if the variable hasn’t been defined, because its value is implicitly <code>undefined</code>.
|Code=// foo variable is not defined
if (typeof foo === "undefined") {
    // executes
}

if (foo === undefined) {
    // throws ReferenceError
}
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The <code>undefined</code> constant is a member of the '''Global''' object, and becomes available when the scripting engine is initialized. When a variable has been declared but not initialized, its value is <code>undefined</code>.

If a variable has not been declared, you cannot compare it to <code>undefined</code> , but you can compare the type of the variable to the string <code>"undefined"</code>. (see second example)

The <code>undefined</code> constant is useful when explicitly testing or setting a variable to <code>undefined</code>.
}}
{{Notes_Section
|Usage='''undefined''' is not a reserved word, thus can be used as a variable in any scope except for the global scope.
|Notes==='''undefined''' vs. '''null'''==
'''undefined''' means a value is declared but not initialized, it doesn't have a value assigned to it.

[[javascript/null{{!}}null]] can be assigned to a variable to represent no value.

Other than that, <code>undefined</code> is a type, while <code>null</code> is an object
|Import_Notes=
}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/operators/typeof{{!}}typeof Operator]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dae3sbk5(v=vs.94).aspx
|HTML5Rocks_link=
}}