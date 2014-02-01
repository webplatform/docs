{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the names of the enumerable properties and methods of an object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Object.keys( object )}}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=The object that contains the properties and methods. This can be an object that you created or an existing Document Object Model (DOM) object.}}
}}
{{JS_Return_Value
|Description=An array that contains the names of the enumerable properties and methods of the object.}}
==Exceptions==
If the value supplied for the object argument is not the name of an object, a TypeError exception is thrown.
{{Remarks_Section
|Remarks=The '''keys''' method returns only the names of enumerable properties and methods. To return the names of both enumerable and non-enumerable properties and methods, you can use [[javascript/Object/getOwnPropertyNames{{!}}Object.getOwnPropertyNames Function]].

For information about the enumerable attribute of a property, see [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]] and [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example creates an object that has three properties and a method. It then uses the '''keys''' method to get the properties and methods of the object.

|Code= // Create a constructor function.
 function Pasta(grain, width, shape) {
     this.grain = grain;
     this.width = width;
     this.shape = shape;
 
     // Define a method.
     this.toString = function () {
         return (this.grain + ", " + this.width + ", " + this.shape);
     }
 }
 
 // Create an object.
 var spaghetti = new Pasta("wheat", 0.2, "circle");
 
 // Put the enumerable properties and methods of the object in an array.
 var arr = Object.keys(spaghetti);
 document.write (arr);
 
 // Output:
 // grain,width,shape,toString
}}{{Single_Example
|Language=JavaScript
|Description=The following example displays the names of all enumerable properties that start with the letter "g" in the Pasta object.

|Code= // Create a constructor function.
 function Pasta(grain, width, shape) {
     this.grain = grain;
     this.width = width;
     this.shape = shape;
 }
 
 var polenta = new Pasta("corn", 1, "mush");
 
 var keys = Object.keys(polenta).filter(CheckKey);
 document.write(keys);
 
 // Check whether the first character of a string is "g".
 function CheckKey(value) {
     var firstChar = value.substr(0, 1);
     if (firstChar.toLowerCase() == "g")
         return true;
     else
         return false;
 }
 
 // Output:
 // grain
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/getOwnPropertyNames{{!}}Object.getOwnPropertyNames Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff688127(v=vs.94).aspx
|HTML5Rocks_link=
}}