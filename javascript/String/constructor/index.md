{{Page_Title}}
{{Flags}}
{{Summary_Section|Specifies the function that creates a string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= string.constructor}}
}}
{{Remarks_Section
|Remarks=The required string is the name of a string.

The '''constructor''' property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the '''Global''' and '''Math''' objects. The '''constructor''' property contains a reference to the function that constructs instances of that particular object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.

|Code= var x = new String();
 
 if (x.constructor == String)
     document.write("Object is a String.");
 else
     document.write("Object is not a String.");
 
 // Output:
 // Object is a String.
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155297(v=vs.94).aspx
|HTML5Rocks_link=
}}