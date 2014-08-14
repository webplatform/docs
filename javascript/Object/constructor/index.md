{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Specifies the function that creates an object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=object.constructor
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.
|Code=// A constructor function.
 function MyObj() {
     this.number = 1;
 }
 
 var x = new String("Hi");
 
 if (x.constructor == String)
     document.write("Object is a String.");
 document.write ("&lt;br /&gt;");
 
 var y = new MyObj;
 if (y.constructor == MyObj)
     document.write("Object constructor is MyObj.");
 
 // Output:
 // Object is a String.
 // Object constructor is MyObj.
}}
}}
{{Remarks_Section
|Remarks=The required object is the name of an object or function.

The '''constructor''' property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the '''Global''' and '''Math''' objects. The '''constructor''' property contains a reference to the function that constructs instances of that particular object.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/prototype{{!}}prototype Property (Object)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/c1hcx253(v=vs.94).aspx
|HTML5Rocks_link=
}}