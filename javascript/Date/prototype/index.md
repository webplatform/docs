{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a reference to the prototype for a date.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= date.prototype}}
}}
{{Remarks_Section
|Remarks=The date argument is the name of an object.

Use the '''prototype''' property to provide a base set of functionality to a Date. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the '''Date''' object that returns the value of the largest element of the array, declare the function, add it to '''Date.prototype''' , and then use it.

 function max( ){
     var max = new Date();
     max.setFullYear(2200, 01, 01);
     return max;
 }
 Date.prototype.maxDate = max;
 var myDate = new Date();
 
 if (myDate &lt; myDate.maxDate())
     document.write("today isn't the max");
 else if (myDate == myDate.maxDate())
     document.write("today is the max"); 
 
 // Output:
 // today isn't the max
All intrinsic JavaScript objects have a '''prototype''' property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155281(v=vs.94).aspx
|HTML5Rocks_link=
}}