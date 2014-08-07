{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a reference to the prototype for a class of string.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=string.prototype
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The string argument is the name of a string.

Use the '''prototype''' property to provide a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the '''String''' object that returns the value of the last element of the string, declare the function, add it to '''String.prototype''' , and then use it.

|Code=function string_last( ){
    return this.charAt(this.length - 1);
}
String.prototype.last = string_last;
var myString = new String("every good boy does fine");
document.write(myString.last());
 
// Output:
// e
}}
}}
{{Remarks_Section
|Remarks=All intrinsic JavaScript objects have a '''prototype''' property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155280(v=vs.94).aspx
|HTML5Rocks_link=
}}