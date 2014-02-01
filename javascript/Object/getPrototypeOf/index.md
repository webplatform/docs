{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the prototype of an object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Object.getPrototypeOf( object )}}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=The object that references the prototype.}}
}}
{{JS_Return_Value
|Description=The prototype of the object argument. The prototype is also an object.}}
==Exceptions==
If the object argument is not an object, a TypeError exception is thrown.
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Object.getPrototypeOf''' function.

|Code= // Create a constructor function.
 function Pasta(grain, width) {
     this.grain = grain;
     this.width = width;
 }
 // Create an object from the pasta constructor.
 var spaghetti = new Pasta("wheat", 0.2);
 
 // Obtain the prototype from the object.
 var proto = Object.getPrototypeOf(spaghetti);
 
 // Add a property to the prototype and validate that
 // the original object has the property.
 proto.foodgroup = "carbohydrates";
 document.write(spaghetti.foodgroup + " ");
 
 // Verify that the prototype obtained from the object
 // is the same as the prototype of the constructor.
 var result = (proto === Pasta.prototype);
 document.write(result + " ");
 
 // Verify that prototype obtained from the object
 // is a prototype of the original object.
 var result = proto.isPrototypeOf(spaghetti);
 document.write(result);
 
 // Output: carbohydrates true true
}}{{Single_Example
|Language=JavaScript
|Description=The following example uses the '''Object.getPrototypeOf''' function to validate data types.

|Code= var reg = /a/;
 var result = (Object.getPrototypeOf(reg) === RegExp.prototype);
 document.write(result + " ");
 
 var err = new Error("an error");
 var result = (Object.getPrototypeOf(err) === Error.prototype);
 document.write(result);
 
 // Output: true true
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/prototype{{!}}prototype Property (Object)]]
* [[javascript/Object/isPrototypeOf{{!}}isPrototypeOf Method (Object)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff877835(v=vs.94).aspx
|HTML5Rocks_link=
}}