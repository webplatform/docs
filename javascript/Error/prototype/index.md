{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a reference to the prototype for an error.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=error.prototype
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=For example, to add a method to the '''Error''' object that returns the value of the largest element of the array, declare the function, add it to '''Error.prototype''' , and then use it.

|Code= function getSeverity(){
     if (this.number &gt; 1000)
         return "high";
     else
         return "low";
 }
 Error.prototype.getSev = getSeverity;
 var myError = new Error();
 myError.number = 5000;
 
 document.write(myError.getSev()); 
 
 // Output: high
}}
}}
{{Remarks_Section
|Remarks=The error argument is the name of an error.

Use the '''prototype''' property to provide a base set of functionality to an Error. New instances of an object "inherit" the behavior of the prototype assigned to that object.

All intrinsic JavaScript objects have a '''prototype''' property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155286(v=vs.94).aspx
|HTML5Rocks_link=
}}