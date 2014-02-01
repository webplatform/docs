{{Page_Title}}
{{Flags}}
{{Summary_Section|Creates a new function.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= function functionName '''([''' argname1  [, ...[, argnameN ]]])}}{{JS_Syntax_Format
|Format= {}}{{JS_Syntax_Format
|Format=     body }}{{JS_Syntax_Format
|Format= }}}{{JS_Syntax_Format
|Format= functionName = new Function( [ argname1 ,  [... argnameN ,]] body );}}
|Values={{JS_Syntax_Parameter
|Name=functionName
|Required=Required
|Description=The name of the newly created function}}{{JS_Syntax_Parameter
|Name=argname1...argnameN
|Required=Optional
|Description=A list of arguments the function accepts.}}{{JS_Syntax_Parameter
|Name=body
|Required=Optional
|Description=A string that contains the block of JavaScript code to be executed when the function is called.}}
}}
{{Remarks_Section
|Remarks=The function is a basic data type in JavaScript. Syntax 1 creates a function value that JavaScript converts into a Function object when necessary. JavaScript converts Function objects created by Syntax 2 into function values at the time the function is called.

Syntax 1 is the standard way to create new functions in JavaScript. Syntax 2 is an alternative form used to create function objects explicitly.

For example, to declare a function that adds the two arguments passed to it, you can do it in one of two ways:
}}
==Example 1==
 function add(x, y)
 {
    return(x + y);
 }
==Example 2==
 var add = function(x, y) {
      return(x+y);
 }
In either case, you call the function with a line of code similar to the following:

 add(2, 3);
'''Note''' -- When you call a function, make sure that you always include the parentheses and any required arguments. Calling a function without parentheses causes the function itself to be returned, instead of the return value of the function.
==Properties==
[[javascript/arguments/0 n Properties|prototype Property]]
==Methods==
[[javascript/Function/apply|valueOf Method]]
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
* [[javascript/operators/new{{!}}new Operator]]
* [[javascript/statements/var{{!}}var Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/x844tc74(v=vs.94).aspx
|HTML5Rocks_link=
}}