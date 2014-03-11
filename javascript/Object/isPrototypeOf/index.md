{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Determines whether an object exists in another object's prototype chain.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=isPrototypeOf( object2 )
}}
|Values={{JS Syntax Parameter
|Name=object2
|Required=Required
|Description=Another object whose prototype chain is to be checked.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''isPrototypeOf''' method.
|Code=var re = new RegExp();
 document.write(RegExp.prototype.isPrototypeOf(re));
 
 // Output: true
}}
}}
{{Remarks_Section
|Remarks=The '''isPrototypeOf''' method returns true if object2 has object1 in its prototype chain. The prototype chain is used to share functionality between instances of the same object type. The '''isPrototypeOf''' method returns false when object2 is not an object or when object1 does not appear in the prototype chain of the object2.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.6 15.2.4.6 Object.prototype.isPrototypeOf (V)]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Array
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/bch72c9e(v=vs.94).aspx
|HTML5Rocks_link=
}}