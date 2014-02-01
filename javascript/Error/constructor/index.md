{{Page_Title}}
{{Flags}}
{{Summary_Section|Specifies the function that creates an Error.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= error.constructor}}
}}
{{Remarks_Section
|Remarks=The required error is the name of an error object.

The '''constructor''' property is a member of the prototype of every object that has a prototype. The '''constructor''' property contains a reference to the function that constructs instances of that particular object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.

|Code= var x = new Error("This is an error");
 
 if (x.constructor == Error)
     document.write("Object is an error.");
 
 // Output:
 // Object is an error.
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155181(v=vs.94).aspx
|HTML5Rocks_link=
}}