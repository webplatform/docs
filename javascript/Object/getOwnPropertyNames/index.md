{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the names of the own properties of an object. The own properties of an object are those that are defined directly on that object, and are not inherited from the object's prototype. The properties of an object include both fields (objects) and functions.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Object.getOwnPropertyNames( object )
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=The object that contains the own properties.
}}
}}
{{JS_Return_Value
|Description=An array that contains the names of the own properties of the object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example creates an object that has three properties and a method. It then uses the '''getOwnPropertyNames''' method to obtain the own properties (including the method) of the object.
|Code=function Pasta(grain, width, shape) {
     // Define properties.
     this.grain = grain;
     this.width = width;
     this.shape = shape;
     this.toString = function () {
         return (this.grain + ", " + this.width + ", " + this.shape);
     }
 }
 
 // Create an object.
 var spaghetti = new Pasta("wheat", 0.2, "circle");
 
 // Get the own property names.
 var arr = Object.getOwnPropertyNames(spaghetti);
 document.write (arr);
 
 // Output:
 //   grain,width,shape,toString
}}{{Single Example
|Language=JavaScript
|Description=The following example displays the names of properties that start with the letter 's' in a spaghetti object constructed with the Pasta constructor.
|Code=function Pasta(grain, size, shape) {
     this.grain = grain; 
     this.size = size; 
     this.shape = shape; 
 }
 
 var spaghetti = new Pasta("wheat", 2, "circle");
 
 var names = Object.getOwnPropertyNames(spaghetti).filter(CheckKey);
 document.write(names); 
 
 // Check whether the first character of a string is 's'. 
 function CheckKey(value) {
     var firstChar = value.substr(0, 1); 
     if (firstChar.toLowerCase() == 's')
         return true; 
     else
          return false; 
 }
 // Output:
 // size,shape
}}
}}
{{Remarks_Section
|Remarks=The '''getOwnPropertyNames''' method returns the names of both enumerable and non-enumerable properties and methods. To return only the names of enumerable properties and methods, you can use the [[javascript/Object/keys{{!}}Object.keys Function]].
}}
{{Notes_Section}}
{{JS Object Listing}}
==Exceptions==
If the value supplied for the object argument is not the name of an object, a TypeError exception is thrown.



{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/keys{{!}}Object.keys Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff688126(v=vs.94).aspx
|HTML5Rocks_link=
}}