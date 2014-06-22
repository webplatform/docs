{{Page_Title}}
{{Flags
|State=Not Ready
|Checked_Out=No
}}
{{Summary_Section|Returns a string that identifies the data type of an expression.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''typeof''' [ '''(''' ] expression [ ''')''' ] ;
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example tests the data type of variables.
|Code=var index = 5;
 var result = (typeof index === 'number');
 // Output: true
 
 var description = "abc";
 var result = (typeof description === 'string');
 // Output: true
}}{{Single Example
|Language=JavaScript
|Description=The following example tests for a data type of undefined for declared and undeclared variables.
|Code=var declared;
 var result = (declared === undefined);
 // Output: true
 
 var result = (typeof declared === 'undefined');
 // Output: true
 
 var result = (typeof notDeclared === 'undefined')
 // Output: true
 
 var obj = {};
 var result = (typeof obj.propNotDeclared === 'undefined');
 // Output: true
 
 // An undeclared variable cannot be compared to undefined,
 // so the next line generates an error.
 //  var result = (notDeclared === undefined);
}}
}}
{{Remarks_Section
|Remarks=The expression argument is any expression for which type information is sought.

The typeof operator returns type information as a string. There are six possible values that typeof returns: "number," "string," "boolean," "object," "function," and "undefined."

The parentheses are optional in the typeof syntax.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Array/isArray{{!}}Array.isArray Function]]
* [[javascript/Object/getPrototypeOf{{!}}Object.getPrototypeOf Function]]
* [[javascript/undefined{{!}}undefined Constant]]
* [[javascript/operators/comparison{{!}}Comparison Operators]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/259s7zc1(v=vs.94).aspx
|HTML5Rocks_link=
}}