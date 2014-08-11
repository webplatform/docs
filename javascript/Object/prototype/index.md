{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a reference to the prototype for a class of objects.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=objectName.prototype
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The objectName argument is the name of an object.

Use the '''prototype''' property to provide a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the '''Array''' object that returns the value of the largest element of the array, declare the function, add it to '''Array.prototype''' , and then use it.

|Code=function array_max( ){
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
 
 // Output:
 // 25
}}
}}
{{Remarks_Section
|Remarks=All intrinsic JavaScript objects have a '''prototype''' property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/constructor{{!}}constructor Property (Object)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/f5s9ycex(v=vs.94).aspx
|HTML5Rocks_link=
}}