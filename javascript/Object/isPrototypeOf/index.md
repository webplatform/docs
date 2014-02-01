{{Page_Title}}
{{Flags}}
{{Summary_Section|Determines whether an object exists in another object's prototype chain.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= object1. isPrototypeOf( object2 )}}
|Values={{JS_Syntax_Parameter
|Name=object1
|Required=Required
|Description=Instance of an object.}}{{JS_Syntax_Parameter
|Name=object2
|Required=Required
|Description=Another object whose prototype chain is to be checked.}}
}}
{{Remarks_Section
|Remarks=The '''isPrototypeOf''' method returns true if object2 has object1 in its prototype chain. The prototype chain is used to share functionality between instances of the same object type. The '''isPrototypeOf''' method returns false when object2 is not an object or when object1 does not appear in the prototype chain of the object2.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''isPrototypeOf''' method.

|Code= var re = new RegExp();
 document.write(RegExp.prototype.isPrototypeOf(re));
 
 // Output: true
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/prototype{{!}}prototype Property (Object)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/bch72c9e(v=vs.94).aspx
|HTML5Rocks_link=
}}