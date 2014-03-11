{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns a reference to the prototype for a Boolean.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=boolean.prototype
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Defines a function and then adds it to Boolean.prototype
|Code= function isFalse( ){
     if (this.toString() == "false")
          return true;
     else
         return false;
 }
 Boolean.prototype.isFalse = isFalse;
 var bool = new Boolean(1);
 document.write(bool.isFalse());
 
 // Output:
 // false
}}{{Single Example
|Language=JavaScript
|Description=Adds a function directly to the Boolean object through its prototype
|Code=//Creates a toggle function for Boolean objects
// through its prototype. All new boolean objects will
// have this method.
Boolean.prototype.toggle = function (){
  return !this.valueOf();
}

}}
}}
{{Remarks_Section
|Remarks=The boolean argument is the name of an object.

The '''prototype''' property provides a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object. Properties and methods may be added to the prototype, but builtin objects may not be assigned a different prototype.

For example, to add a method to the '''Boolean''' object that returns the value of the largest element of the array, declare the function, add it to '''Boolean.prototype''' , and then use it.

}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Property
|Applies to=Boolean
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155296(v=vs.94).aspx
|HTML5Rocks_link=
}}