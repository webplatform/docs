{{Page_Title}}
{{Flags}}
{{Summary_Section|Creates an object that has the specified prototype, and that optionally contains specified properties.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Object.create( prototype , descriptors )}}
|Values={{JS_Syntax_Parameter
|Name=prototype
|Required=Required
|Description=The object to use as a prototype. May be null.}}{{JS_Syntax_Parameter
|Name=descriptors
|Required=Optional
|Description=A JavaScript object that contains one or more property descriptors.A data property is a property that can get and set a value. A data property descriptor contains a value attribute, plus writable , enumerable , and configurable attributes. If the last three attributes are not specified, they default to false. An accessor property calls a user-provided function every time the value is retrieved or set. An accessor property descriptor contains a set attribute, a get attribute, or both. For more information, see [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]].}}
}}
{{JS_Return_Value
|Description=A new object that has the specified internal prototype and contains the specified properties, if any.}}
==Exceptions==
A TypeError exception is thrown if any of the following conditions is true:

* The prototype argument is not an object and is not null.
* A descriptor in the descriptors argument has a value or writable attribute, and has a get or set attribute.
* A descriptor in the descriptors argument has a get or set attribute that is not a function.
{{Remarks_Section
|Remarks=You can use this function using a null prototype parameter in order to stop the prototype chain. The object created will have no prototype.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example creates an object using a null prototype and adds two enumerable properties.

|Code= var newObj = Object.create(null, {
             size: {
                 value: "large",
                 enumerable: true
             },
             shape: {
                 value: "round",
                 enumerable: true
             }
         });
 
 document.write(newObj.size + "&lt;br/&gt;");
 document.write(newObj.shape + "&lt;br/&gt;");
 document.write(Object.getPrototypeOf(newObj));
 
 // Output:
 // large
 // round
 // null
}}{{Single_Example
|Language=JavaScript
|Description=The following example creates an object that has the same internal prototype as the Object object. You can see that it has the same prototype as an object created by using an object literal. The [[javascript/Object/getPrototypeOf{{!}}Object.getPrototypeOf]] function gets the prototype of the original object. To get the object's property descriptor, you can use [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]].

|Code= var firstLine = { x: undefined, y: undefined };
 
 var secondLine = Object.create(Object.prototype, {
         x: {
                 value: undefined, 
                 writable: true, 
                 configurable: true, 
                 enumerable: true
             },
             y: {
                 value: undefined, 
                 writable: true, 
                 configurable: true, 
                 enumerable: true
             }
 });
 
 var firstLine = { x: undefined, y: undefined };
 
 var secondLine = Object.create(Object.prototype, {
         x: {
                 value: undefined, 
                 writable: true, 
                 configurable: true, 
                 enumerable: true
             },
             y: {
                 value: undefined, 
                 writable: true, 
                 configurable: true, 
                 enumerable: true
             }
 });
 
 document.write("first line prototype = " + Object.getPrototypeOf(firstLine));
 document.write("&lt;br/&gt;");
 document.write("second line prototype = " + Object.getPrototypeOf(secondLine));
 
 // Output:
 // first line prototype = [object Object]
 // second line prototype = [object Object]
}}{{Single_Example
|Language=JavaScript
|Description=The following example creates an object that has the same internal prototype as the Shape object.

|Code= // Create the shape object.
 var Shape = { twoDimensional: true, color: undefined, hasLineSegments: undefined };
 
 var Square = Object.create(Object.getPrototypeOf(Shape));
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/getPrototypeOf{{!}}Object.getPrototypeOf Function]]
* [[javascript/Object/isPrototypeOf{{!}}isPrototypeOf Method (Object)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff925952(v=vs.94).aspx
|HTML5Rocks_link=
}}