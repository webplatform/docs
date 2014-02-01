{{Page_Title}}
{{Flags}}
{{Summary_Section|Determines whether an object is an array.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Array.isArray( object )}}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=The object to test.}}
}}
{{JS_Return_Value
|Description=true if object is an array; otherwise, false. If the object argument is not an object, false is returned.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Array.isArray''' function.

|Code= var ar = [];
 var result = Array.isArray(ar);
 // Output: true
 
 var ar = new Array();
 var result = Array.isArray(ar);
 // Output: true
 
 var ar = [1, 2, 3];
 var result = Array.isArray(ar);
 // Output: true
 
 var result = Array.isArray("an array");
 document.write(result);
 // Output: false
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Array{{!}}Array Object]]
* [[javascript/operators/typeof{{!}}typeof Operator]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff848265(v=vs.94).aspx
|HTML5Rocks_link=
}}