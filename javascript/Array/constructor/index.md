{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Specifies the function that creates an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=array.constructor
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.
|Code=var x = new Array();
 
 if (x.constructor == Array)
     document.write("Object is an Array.");
 else
     document.write("Object is not an Array.");
 
 // Output:
 // Object is an Array.
}}
}}
{{Remarks_Section
|Remarks=The required array is the name of an array.

The '''constructor''' property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the '''Global''' and '''Math''' objects. The '''constructor''' property contains a reference to the function that constructs instances of that particular object.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Property
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155291(v=vs.94).aspx
|HTML5Rocks_link=
}}