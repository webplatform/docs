{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add example
|Checked_Out=No
}}
{{Summary_Section|Returns a reference to the prototype for a class of array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Array.prototype
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=The array argument is the name of an array.

Use the '''prototype''' property to provide a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the '''Array''' object that returns the value of the largest element of the array, declare the function, add it to '''Array.prototype''' , and then use it.

 function array_max( ){
     var i, max = this[0];
     for (i = 1; i &lt; this.length; i++)
     {
     if (max &lt; this[i])
     max = this[i];
     }
     return max;
 }
 Array.prototype.max = array_max;
 var myArray = new Array(7, 1, 3, 11, 25, 9
 );
 document.write(myArray.max());
 
 // Output: 25
All intrinsic JavaScript objects have a '''prototype''' property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.
}}
{{Notes_Section
|Import_Notes===Requirements==
Supported in the following document modes: Quirks, Internet Explorer 6 standards, Internet Explorer 7 standards, Internet Explorer 8 standards, Internet Explorer 9 standards, Internet Explorer 10 standards, Internet Explorer 11 standards. Also supported in Windows Store apps. See Version Information.
}}
{{JS Object Listing}}

{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Property
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155285(v=vs.94).aspx
|HTML5Rocks_link=
}}