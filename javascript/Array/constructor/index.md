{{Page_Title}}
{{Flags}}
{{Summary_Section|Specifies the function that creates an array.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= array.constructor}}
}}
{{Remarks_Section
|Remarks=The required array is the name of an array.

The '''constructor''' property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the '''Global''' and '''Math''' objects. The '''constructor''' property contains a reference to the function that constructs instances of that particular object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.

|Code= var x = new Array();
 
 if (x.constructor == Array)
     document.write("Object is an Array.");
 else
     document.write("Object is not an Array.");
 
 // Output:
 // Object is an Array.
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155291(v=vs.94).aspx
|HTML5Rocks_link=
}}