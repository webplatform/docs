{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|The void operator evaluates an expression and then returns <b>undefined</b>.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=void expression
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In this example, <code>void(0)</code> is used to return <code>undefined</code> to the link's <code>href</code> property, so that the browser will not attempt to load a URL and the function in the <code>onclick</code> event can be executed instead.
|Code=<!DOCTYPE html>  
<html>  
<head>  
<title>JavaScript void example</title>  
</head>  
<body> 
<a href="javascript:void(0)" onclick="myFunction()">Click here to execute the function.</a>  
</body>  
</html>
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The expression argument is any valid JavaScript expression.

The void operator evaluates its expression and returns undefined. It is useful in situations where an expression should be evaluated but you do not want a result returned to the rest of the script.

Void works only on unary expressions, thus: <code> void x, y; </code>
will set only the x variable to <b>undefined</b>.
}}
{{Notes_Section
|Usage=
|Notes=void(0) is equivalent to void 0 and returns the <b>undefined</b> value.
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/e17c7cbe(v=vs.94).aspx
|HTML5Rocks_link=
}}