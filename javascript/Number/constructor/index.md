{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Specifies the function that creates a Number.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=number.constructor
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.
|Code=var num = new Number();
 
 if (num.constructor == Number)
     document.write("Object is a Number.");
 else
     document.write("Object is not a Number.");
 
 // Output:
 // Object is a Number.
}}
}}
{{Remarks_Section
|Remarks=The required number is the name of a string.

The '''constructor''' property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the '''Global''' and '''Math''' objects. The '''constructor''' property contains a reference to the function that constructs instances of that particular object.
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj159602(v=vs.94).aspx
|HTML5Rocks_link=
}}