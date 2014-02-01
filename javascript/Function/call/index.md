{{Page_Title}}
{{Flags}}
{{Summary_Section|Calls a method of an object, substituting another object for the current object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= call([ thisObj [, arg1 [ , arg2 [ ,   [ , argN ]]]]])}}
|Values={{JS_Syntax_Parameter
|Name=thisObj
|Required=Optional
|Description=The object to be used as the current object.}}{{JS_Syntax_Parameter
|Name=arg1, arg2, , argN
|Required=Optional
|Description=A list of arguments to be passed to the method.}}
}}
{{Remarks_Section
|Remarks=The '''call''' method is used to call a method on behalf of another object. It allows you to change the this object of a function from the original context to the new object specified by thisObj.

If thisObj is not supplied, the global object is used as thisObj.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to use the '''call''' method.

|Code= function callMe(arg1, arg2){
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
 
 document.write("Function called with call: &lt;br/&gt;");
 document.write(callMe.call(3, 4, 5));
 
 // Output: 
 // Original function: 
 // this value: [object Window]
 // arguments: 1
 // arguments: 2
 
 // Function called with call: 
 // this value: 3
 // arguments: 4
 // arguments: 5
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Function{{!}}Function Object]]
* [[javascript/Function/apply{{!}}apply Method (Function)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/h2ak8h2y(v=vs.94).aspx
|HTML5Rocks_link=
}}