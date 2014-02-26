{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|References the function which created the instance of the Array object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=arrayObj.constructor
}}
|Values={{JS Syntax Parameter
|Name=arrayObj
|Required=Required
|Description=Any Array object.
}}
}}
{{JS_Return_Value
|Description=The function object which constructed the Array instance.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.
|Code=var x = new Array();
 
 if (x.constructor == Array)
     document.write("Object is an Array.");
 else
     document.write("Object is not an Array.");
 
 // Output:
 // Object is an Array.
|LiveURL=http://code.webplatform.org/gist/9237139
}}
}}
{{Remarks_Section
|Remarks=The required array is the name of an array.

The '''constructor''' property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the '''Global''' and '''Math''' objects. If the JavaScript interpreter falls back to their prototype object, the '''constructor''' property references the native <code>Object.prototype.constructor</code>.

 var my_obj = Math;
 document.write(my_obj.constructor === Math);
 
 // Output: false

The '''constructor''' property is only read-only for primitive values such as 1, true and "test".

 var my_obj = new Number(100);
 my_obj.constructor = String; // overwritten
 document.write(my_obj.constructor);
 
 // Output: function String() { [native code] }
 
 my_obj = 100;
 my_obj.constructor = String; // can't be overwritten
 document.write(my_obj.constructor);
 
 // Output: function Number() { [native code] }
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript JavaScript, by Mozilla Developer Network]
* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/constructor Object.prototype.constructor, by Mozilla Developer Network]

|Manual_sections====Specification===
* [http://www.ecma-international.org/ecma-262/5.1/#sec-4.3.4 4.3.4 constructor]
* [http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.1 15.2.4.1 Object.prototype.constructor]

ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Property
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155291(v=vs.94).aspx
|HTML5Rocks_link=
}}