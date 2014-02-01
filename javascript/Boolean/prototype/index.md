{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a reference to the prototype for a Boolean.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= boolean.prototype}}
}}
{{Remarks_Section
|Remarks=The boolean argument is the name of an object.

The '''prototype''' property provides a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object. Properties and methods may be added to the prototype, but builtin objects may not be assigned a different prototype.

For example, to add a method to the '''Boolean''' object that returns the value of the largest element of the array, declare the function, add it to '''Array.prototype''' , and then use it.

 function isFalse( ){
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
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155296(v=vs.94).aspx
|HTML5Rocks_link=
}}