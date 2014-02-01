{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a reference to the prototype for a class of number.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= number.prototype}}
}}
{{Remarks_Section
|Remarks=The number argument is the name of a number.

Use the '''prototype''' property to provide a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the '''Number''' object that returns the number of (integer) digits, declare the function, add it to '''Number.prototype''' , and then use it.

 function number_digits() {
     var digits = 0;
     var num = this;
     while (num) &gt;= 1) {
         digits++;
         num /= 10;
     }
     return digits;
 }
 
 Number.prototype.digits = number_digits;
 var myNumber = new Number(3456.789);
 document.write(myNumber.digits());
 // Output:
 // 4
All intrinsic JavaScript objects have a '''prototype''' property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj159612(v=vs.94).aspx
|HTML5Rocks_link=
}}