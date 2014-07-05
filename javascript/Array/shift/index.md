{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add example
|Checked_Out=No
}}
{{Summary_Section|Removes the first element from an array and returns it.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=shift( )
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns the element removed from the array.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=The following example illustrates the use of the shift method.

 var arr = new Array(10, 11, 12);
 while (arr.length &gt; 0)
     {
     var i = arr.shift();
     document.write (i.toString() + " ");
     }
 
 // Output: 
 // 10 11 12
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.9 15.4.4.9 Array.prototype.shift ( )]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9e7b4w20(v=vs.94).aspx
|HTML5Rocks_link=
}}