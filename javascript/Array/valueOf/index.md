{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns the primitive value of the specified object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=valueOf()
}}
|Values=
}}
{{JS_Return_Value
|Description=Returns the array instance.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In the following example, the instantiated array object is the same as the return value of this method.
|Code=
 var arr = [1, 2, 3, 4];
 var s = arr.valueOf();
 
 if (arr === s)
 document.write("same");
 else
 document.write("different");
 
 // Output:
 // same
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.4 15.2.4.4 Object.prototype.valueOf ( )]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155290(v=vs.94).aspx
|HTML5Rocks_link=
}}