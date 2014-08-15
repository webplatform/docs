{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Calls the function, substituting the specified object for the this value of the function, and the specified array for the arguments of the function.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=apply([ thisObj [, argArray ]])
}}
|Values={{JS Syntax Parameter
|Name=thisObj
|Required=Optional
|Description=The object to be used as the this object.
}}{{JS Syntax Parameter
|Name=argArray
|Required=Optional
|Description=A set of arguments to be passed to the function.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to use the apply method.
|Code=function callMe(arg1, arg2){
     var s = "";
 
     s += "this value: " + this;
     s += "&lt;br /&gt;";
     for (i in callMe.arguments) {
         s += "arguments: " + callMe.arguments[i];
         s += "&lt;br /&gt;";
     }
     return s;
 }
 
 document.write("Original function: &lt;br/&gt;");
 document.write(callMe(1, 2));
 document.write("&lt;br/&gt;");
 
 document.write("Function called with apply: &lt;br/&gt;");
 document.write(callMe.apply(3, [ 4, 5 ]));
 
 // Output: 
 // Original function: 
 // this value: [object Window]
 // arguments: 1
 // arguments: 2
 
 // Function called with apply: 
 // this value: 3
 // arguments: 4
 // arguments: 5
}}
}}
{{Remarks_Section
|Remarks=If argArray is not a valid object, then an "Object expected" error occurs.

If neither argArray nor thisObj are supplied, the original this object is used as thisObj and no arguments are passed.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Function{{!}}Function Object]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/4zc42wh1(v=vs.94).aspx
|HTML5Rocks_link=
}}