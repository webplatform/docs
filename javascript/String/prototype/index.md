{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a reference to the prototype for a class of string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= string.prototype}}
}}
{{Remarks_Section
|Remarks=The string argument is the name of a string.

Use the '''prototype''' property to provide a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the '''String''' object that returns the value of the last element of the string, declare the function, add it to '''String.prototype''' , and then use it.

 function string_last( ){
     return this.charAt(this.length - 1);
 }
 String.prototype.last = string_last;
 var myString = new String("every good boy does fine");
 document.write(myString.last());
 
 // Output:
 // e
All intrinsic JavaScript objects have a '''prototype''' property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155280(v=vs.94).aspx
|HTML5Rocks_link=
}}